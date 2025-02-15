# my-first-project
import { motion } from "framer-motion";
import { Heart } from "lucide-react";
import { Card } from "@/components/ui/card";

export default function Home() {
  return (
    <div className="min-h-screen w-full flex items-center justify-center bg-gradient-to-br from-pink-100 to-rose-100 p-4">
      <motion.div
        initial={{ scale: 0.5, opacity: 0 }}
        animate={{ scale: 1, opacity: 1 }}
        transition={{ 
          duration: 0.8,
          type: "spring",
          bounce: 0.4
        }}
        className="w-full max-w-2xl"
      >
        <Card className="p-8 shadow-xl bg-white/90 backdrop-blur">
          <motion.div
            initial={{ y: 20, opacity: 0 }}
            animate={{ y: 0, opacity: 1 }}
            transition={{ delay: 0.3 }}
            className="flex flex-col items-center gap-6 text-center"
          >
            <motion.div
              animate={{ 
                scale: [1, 1.1, 1],
                rotate: [0, -5, 5, -5, 0]
              }}
              transition={{ 
                duration: 1.5,
                repeat: Infinity,
                repeatDelay: 2
              }}
            >
              <Heart className="w-16 h-16 text-red-500" />
            </motion.div>

            <div className="space-y-4">
              <h1 className="text-3xl md:text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-pink-600">
                Bạn đã bị lừa vào cạm bẫy tình iu của đội TNTN!
              </h1>

              <motion.div 
                className="text-2xl md:text-3xl font-semibold text-rose-600"
                initial={{ opacity: 0, y: 20 }}
                animate={{ opacity: 1, y: 0 }}
                transition={{ delay: 0.6 }}
              >
                Bạn phải thanh toán 20k cho dịch vụ nè!
                <div className="text-lg mt-2 font-normal text-gray-600">
                  STK: 100883030407
                </div>
              </motion.div>
            </div>
          </motion.div>
        </Card>
      </motion.div>
    </div>
  );
}
