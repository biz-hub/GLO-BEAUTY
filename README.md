import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Sparkles, Eye, Brush } from "lucide-react";

const products = [ { name: "Luxe Lashes", image: "https://via.placeholder.com/200x200?text=Lashes", price: "$12.99" }, { name: "Glossy Lips", image: "https://via.placeholder.com/200x200?text=Gloss", price: "$9.99" }, { name: "Pro Brush Set", image: "https://via.placeholder.com/200x200?text=Brush+Set", price: "$19.99" } ];

export default function GloBeautyWebsite() { return ( <div className="min-h-screen bg-pink-50 flex flex-col items-center justify-center px-4 py-10 text-center"> <header className="mb-8"> <h1 className="text-5xl font-bold text-rose-500 font-cursive">Glo-Beauty</h1> <p className="text-xl mt-2 text-rose-400 italic">Let Your Beauty Glow</p> </header>

<Card className="max-w-md w-full bg-white/90 shadow-xl rounded-2xl p-6">
    <CardContent>
      <div className="flex flex-col items-center space-y-4">
        <div className="flex items-center space-x-4">
          <Eye className="text-rose-400 w-8 h-8" />
          <Brush className="text-rose-300 w-8 h-8" />
          <Sparkles className="text-yellow-400 w-8 h-8" />
        </div>
        <p className="text-gray-700 text-lg">
          Discover premium lashes, glosses, and brushes designed to let your beauty glow from within.
        </p>
        <Button className="bg-rose-500 hover:bg-rose-600 text-white rounded-full px-6 py-2 text-lg">
          Shop Now
        </Button>
      </div>
    </CardContent>
  </Card>

  <section className="mt-12 w-full max-w-5xl">
    <h2 className="text-3xl font-semibold text-rose-400 mb-6">Our Products</h2>
    <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      {products.map((product, index) => (
        <Card key={index} className="bg-white shadow-md rounded-xl p-4">
          <img src={product.image} alt={product.name} className="w-full h-48 object-cover rounded-lg mb-4" />
          <h3 className="text-lg font-semibold text-rose-500">{product.name}</h3>
          <p className="text-sm text-gray-600">{product.price}</p>
          <Button className="mt-3 bg-rose-500 hover:bg-rose-600 text-white rounded-full px-4 py-1 text-sm">
            Buy Now
          </Button>
        </Card>
      ))}
    </div>
  </section>

  <footer className="mt-10 text-sm text-rose-300">
    &copy; 2025 Glo-Beauty. All rights reserved.
  </footer>
</div>

); }

