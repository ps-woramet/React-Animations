1. aos
    
    https://michalsnik.github.io/aos/

    https://github.com/michalsnik/aos

    -index.html

        <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />

        <body>
            <script src="https://unpkg.com/aos@next/dist/aos.js"></script>
            <script>
            AOS.init();
            </script>
            <div id="root"></div>
            <script type="module" src="/src/main.jsx"></script>
        </body>

    -MyComponent.jsx

        <div data-aos="flip-left">
          <section class="bg-white dark:bg-gray-900">
              <div class="gap-16 items-center py-8 px-4 mx-auto max-w-screen-xl lg:grid lg:grid-cols-2 lg:py-16 lg:px-6">
                <div class="grid grid-cols-2 gap-4 mt-8">
                      <img class="w-full rounded-lg" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/content/office-long-2.png" alt="office content 1"/>
                      <img class="mt-4 w-full lg:mt-10 rounded-lg" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/content/office-long-1.png" alt="office content 2"/>
                  </div>
                  <div class="font-light text-gray-500 sm:text-lg dark:text-gray-400">
                      <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">We didn't reinvent the wheel</h2>
                      <p class="mb-4">We are strategists, designers and developers. Innovators and problem solvers. Small enough to be simple and quick, but big enough to deliver the scope you want at the pace you need. Small enough to be simple and quick, but big enough to deliver the scope you want at the pace you need.</p>
                      <p>We are strategists, designers and developers. Innovators and problem solvers. Small enough to be simple and quick.</p>
                  </div>
            </div>
          </section>
        </div>

2. react-reveal

    https://www.react-reveal.com/examples/common/zoom/

    npm install react-reveal --save

    -MyComponent.jsx

        import Fade from 'react-reveal/Fade';

        <Fade bottom>
            <section class="bg-white dark:bg-gray-900">
                <div class="gap-16 items-center py-8 px-4 mx-auto max-w-screen-xl lg:grid lg:grid-cols-2 lg:py-16 lg:px-6">
                    <div class="font-light text-gray-500 sm:text-lg dark:text-gray-400">
                        <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">We didn't reinvent the wheel</h2>
                        <p class="mb-4">We are strategists, designers and developers. Innovators and problem solvers. Small enough to be simple and quick, but big enough to deliver the scope you want at the pace you need. Small enough to be simple and quick, but big enough to deliver the scope you want at the pace you need.</p>
                        <p>We are strategists, designers and developers. Innovators and problem solvers. Small enough to be simple and quick.</p>
                    </div>
                    <div class="grid grid-cols-2 gap-4 mt-8">
                        <img class="w-full rounded-lg" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/content/office-long-2.png" alt="office content 1"/>
                        <img class="mt-4 w-full lg:mt-10 rounded-lg" src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/content/office-long-1.png" alt="office content 2"/>
                    </div>
            </div>
            </section>
        </Fade>

3. scroll to ref

    https://www.codingbeautydev.com/blog/react-scroll-to-element

    -MyComponent.jsx ทำการใช้ useRef เพื่อเข้าถึง html tag
        
        import React, { useRef } from 'react';

        const ref = useRef(null);

        const handleClick = () => {
            ref.current?.scrollIntoView({ behavior: 'smooth' });
        };

        <div ref={ref} class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700 m-auto">
            <a href="#">
                <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Ps.Woramet</h5>
            </a>
            <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">Woramet Tompudsa</p>
            <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                Read more
                <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                </svg>
            </a>
        </div>

        <div className='flex items-center justify-center my-4'>
          <button onClick={handleClick} class="flex items-center justify-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
            Go to Ps.woramet !
            <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
            </svg>
          </button>
        </div>

4. framer motion

    npm install framer-motion

    -MyComponent.jsx

        import { motion } from "framer-motion";

        <motion.div
            initial={{ opacity: 0, x: -100 }}
            animate={{ opacity: 1, x: 0 }}
            exit={{ opacity: 0, x: 100 }}
            transition={{ duration: 0.5 }}
        >
            <h1 className="flex items-center justify-center text-3xl font-bold p-5">
                React Animation!
            </h1>

        </motion.div>