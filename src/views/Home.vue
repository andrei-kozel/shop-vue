<template>
    <div class="home bg-gray-200 flex flex-wrap justify-center">
        <h1 class="text-6xl w-full mt-8">Perfect Book Store</h1>
        <div v-for="(book, index) in books" :key="index">
            <ProductCard :book="book" />
        </div>
    </div>
</template>

<script>
import ProductCard from '../components/ProductCard'
export default {
    name: 'Home',
    data() {
        return {
            books: [
                {
                    image:
                        'https://images-na.ssl-images-amazon.com/images/I/511vJPN7p5L._SX331_BO1,204,203,200_.jpg',
                    title: 'The Subtle Art of Not Giving a F*ck',
                    rating: 4.5,
                    description: `In this generation-defining self-help guide, a superstar blogger cuts through the crap to show us how to stop trying to be "positive" all the time so that we can truly become better, happier people. \n
                    \n
                    For decades, we 've been told that positive thinking is the key to a happy, rich life. "F**k positivity," Mark Manson says. "Let’s be honest, shit is f**ked and we have to live with it." In his wildly popular Internet blog, Manson doesn’t sugarcoat or equivocate. He tells it like it is—a dose of raw, refreshing, honest truth that is sorely lacking today. The Subtle Art of Not Giving a F**k is his antidote to the coddling, let’s-all-feel-good mindset that has infected American society and spoiled a generation, rewarding them with gold medals just for showing up.\n

                    Manson makes the argument, backed both by academic research and well-timed poop jokes, that improving our lives hinges not on our ability to turn lemons into lemonade, but on learning to stomach lemons better. Human beings are flawed and limited—"not everybody can be extraordinary, there are winners and losers in society, and some of it is not fair or your fault." Manson advises us to get to know our limitations and accept them. Once we embrace our fears, faults, and uncertainties, once we stop running and avoiding and start confronting painful truths, we can begin to find the courage, perseverance, honesty, responsibility, curiosity, and forgiveness we seek.\n

                    There are only so many things we can give a f**k about so we need to figure out which ones really matter, Manson makes clear. While money is nice, caring about what you do with your life is better, because true wealth is about experience. A much-needed grab-you-by-the-shoulders-and-look-you-in-the-eye moment of real-talk, filled with entertaining stories and profane, ruthless humor, The Subtle Art of Not Giving a F**k is a refreshing slap for a generation to help them lead contented, grounded lives.`,
                    price: '49',
                    id: 1
                },
                {
                    image:
                        'https://images-na.ssl-images-amazon.com/images/I/51Fqn4+UodL._SY344_BO1,204,203,200_.jpg',
                    title: 'Atomic Habits',
                    rating: 4.5,
                    description: `People think that when you want to change your life, you need to think big. But world-renowned habits expert James Clear has discovered another way. He knows that real change comes from the compound effect of hundreds of small decisions – doing two push-ups a day, waking up five minutes early, or holding a single short phone call.

                    He calls them atomic habits.

                    In this ground-breaking book, Clears reveals exactly how these minuscule changes can grow into such life-altering outcomes. He uncovers a handful of simple life hacks (the forgotten art of Habit Stacking, the unexpected power of the Two Minute Rule, or the trick to entering the Goldilocks Zone), and delves into cutting-edge psychology and neuroscience to explain why they matter. Along the way, he tells inspiring stories of Olympic gold medalists, leading CEOs, and distinguished scientists who have used the science of tiny habits to stay productive, motivated, and happy.`,
                    price: '65',
                    id: 2
                },
                {
                    image:
                        'https://m.media-amazon.com/images/I/418NnKr2KKL.jpg',
                    title: 'Vue: Step-By-Step ',
                    rating: 3,
                    description: `Vue JS is is a progressive real time framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable.

                    Also, Vue is becoming more popular day by day and thousands of jobs are posting each day.



                    Each chapter will contain a certain number of relevant topics with illustrations and exercises where necessary, for an easy and enjoyable learning.

                    Benefits of this Book/Tutorial you will not find anywhere else:

                    This book will help you to become a master of Vue JS for real
                    This book teaches you Vue JS from beginning to advanced level
                    Also it will show you how to install Vue JS packages step by step as well`,
                    price: '25',
                    id: 3
                },
                {
                    image:
                        'https://images-na.ssl-images-amazon.com/images/I/41iYPb47M-L._SX384_BO1,204,203,200_.jpg',
                    title: 'Fullstack Vue',
                    rating: 4,
                    description: `What if you could master the entire framework - with solid foundations - in less time without beating your head against a wall? Imagine how quickly you could work if you knew the best practices and the best tools?
Stop wasting your time searching and have everything you need to be productive in one, well-organized place, with complete examples to get your project up without needing to resort to endless hours of research.

Lots of Sample Apps and Code

You will learn what you need to know to work professionally with Fullstack Vue: The Complete Guide to Vue.js

You'll build:

A Server-Persisted Shopping Cart: Use the Flux-like library Vuex to manage data for a large shopping cart application that persists information on to a local server.
A Calendar Event App: Dive deeper into component based architecture by learning how simple state management works with Vue Single-file components.
A Voting Application: Learn how to render dynamic components and use standard Vue directives to build an interactive voting application.
Forms with Validations: Build powerful forms that accept user input, and give clear messaging when the input is of an invalid format.
Vuex-based Routes and Authentication: Build on top of the server persisted shopping cart app by creating dynamic routes and a token authentication flow with the official vue-router library.
Build bullet-proof apps with Testing: Use Vue's official test utility library, vue-test-utils, to create meaningful tests for a daily weather app that interacts with a third party API.`,
                    price: '30',
                    id: 4
                }
            ]
        }
    },
    components: {
        ProductCard
    }
}
</script>
