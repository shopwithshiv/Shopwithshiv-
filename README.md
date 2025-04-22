# Shopwithshiv-
Shiv Affiliate Marketing 
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const categories = [
  "मोबाइल / Mobile",
  "फैशन / Fashion",
  "इलेक्ट्रॉनिक्स / Electronics",
  "होम डेकोर / Home Decor",
  "ब्यूटी / हेल्थ / Beauty & Health",
  "किचन / Kitchen",
  "फिटनेस / Fitness"
];

const products = [
  {
    name: "Redmi 13C",
    category: "मोबाइल / Mobile",
    price: "₹7,999",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/81fRAoUL-fL._SX679_.jpg"
  },
  {
    name: "Men's Cotton T-Shirt",
    category: "फैशन / Fashion",
    price: "₹399",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/71FxoXq6FqL._UX569_.jpg"
  },
  {
    name: "boAt Airdopes 141",
    category: "इलेक्ट्रॉनिक्स / Electronics",
    price: "₹1,299",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/61KNJav3S9L._SX679_.jpg"
  },
  {
    name: "Home Decorative Light",
    category: "होम डेकोर / Home Decor",
    price: "₹799",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/71jqa1U9gmL._SY679_.jpg"
  },
  {
    name: "Mamaearth Ubtan Face Wash",
    category: "ब्यूटी / हेल्थ / Beauty & Health",
    price: "₹249",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/61pLZ3FdVUL._SX679_.jpg"
  },
  {
    name: "Prestige Non Stick Pan",
    category: "किचन / Kitchen",
    price: "₹999",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/71YpMts+IOL._SX679_.jpg"
  },
  {
    name: "Kobo Exercise Dumbbells",
    category: "फिटनेस / Fitness",
    price: "₹649",
    link: "https://amzn.to/42IqQlN",
    image: "https://m.media-amazon.com/images/I/71Lo6Wx9-BL._SX679_.jpg"
  }
];

export default function ShopWithShiv() {
  return (
    <div className="p-4">
      <h1 className="text-3xl font-bold text-center mb-6">ShopWithShiv.com</h1>
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
        {products.map((product, index) => (
          <Card key={index} className="rounded-2xl shadow-lg">
            <img
              src={product.image}
              alt={product.name}
              className="rounded-t-2xl w-full h-48 object-cover"
            />
            <CardContent className="p-4">
              <h2 className="text-lg font-semibold mb-2">{product.name}</h2>
              <p className="text-sm mb-1">{product.category}</p>
              <p className="text-md font-bold mb-3">{product.price}</p>
              <a href={product.link} target="_blank" rel="noopener noreferrer">
                <Button className="w-full">Buy Now / अभी खरीदें</Button>
              </a>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}
