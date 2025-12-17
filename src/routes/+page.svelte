<script lang="ts">
	import { onMount } from 'svelte';

	let scrollY = 0;
</script>

<svelte:window bind:scrollY />

<div class="font-sans text-gray-900 antialiased selection:bg-primary-200 selection:text-primary-900">

	<!-- Hero Section -->
	<section class="relative min-h-screen w-full bg-gradient-to-b from-gray-950 via-gray-900 to-white text-white px-6 md:px-12 lg:px-24 pt-32 pb-24 flex flex-col justify-between">
		<!-- Logo -->
		<div class="absolute top-8 left-6 md:left-12 lg:left-24">
			<svg width="80" height="47" viewBox="0 0 116 68" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path fill-rule="evenodd" clip-rule="evenodd" d="M44.6215 56.0343C46.6079 53.651 49.5502 52.2726 52.6531 52.2726H94.8018C106.35 52.2726 115.711 42.9114 115.711 31.3637V20.909C115.711 9.36134 106.35 0 94.8018 0H86.6303C83.5277 0 80.5851 1.37818 78.599 3.76179L71.8003 11.9201C69.814 14.3037 66.8716 15.6818 63.7688 15.6818H21.62C10.0722 15.6818 0.710938 25.043 0.710938 36.5909V47.0454C0.710938 58.5933 10.0722 67.9546 21.62 67.9546H29.7916C32.8942 67.9546 35.8367 66.5765 37.8229 64.1929L44.6215 56.0343ZM100.029 20.909C100.029 18.022 97.6888 15.6818 94.8018 15.6818H78.7895C75.6866 15.6818 72.7443 17.0599 70.7579 19.4435L63.9593 27.602C61.9731 29.9854 59.0306 31.3637 55.9279 31.3637H21.62C18.7331 31.3637 16.3927 33.704 16.3927 36.5909V47.0454C16.3927 49.9324 18.7331 52.2726 21.62 52.2726H37.6324C40.7352 52.2726 43.6776 50.8945 45.664 48.5109L52.4626 40.3526C54.4488 37.969 57.3913 36.5909 60.4939 36.5909H94.8018C97.6888 36.5909 100.029 34.2507 100.029 31.3637V20.909Z" fill="white"/>
			</svg>
		</div>

		<div class="max-w-5xl">
			<h1 class="font-serif text-5xl md:text-7xl lg:text-8xl leading-[1.1] md:leading-[1.1] tracking-tight">
				Transform ideas into production-ready interfaces through AI that reasons about design.
			</h1>
			<p class="text-xl md:text-2xl text-white/70 mt-8 max-w-3xl">
				Not templates. Not guesswork. Real design reasoning that understands structure, hierarchy, and user intent.
			</p>
		</div>

		<div class="mt-24 flex gap-4">
			<a href="#examples" class="inline-flex items-center justify-center px-6 py-3 bg-primary-500 text-white rounded-full text-sm font-medium hover:bg-primary-600 transition-colors duration-300">
				See examples
			</a>
			<a href="#how-it-works" class="inline-flex items-center justify-center px-6 py-3 border border-white/30 rounded-full text-sm font-medium hover:bg-white hover:text-gray-900 transition-colors duration-300 backdrop-blur-sm">
				How it works
			</a>
		</div>
	</section>

	<!-- Trusted By -->
	<section class="bg-white px-6 md:px-12 lg:px-24 py-16 md:py-24">
		<p class="text-lg md:text-xl text-gray-600 mb-12">Trusted by product builders shipping fast</p>
		
		<div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 md:gap-8">
			<!-- Logos placeholders -->
			{#each ['Linear', 'Vercel', 'Stripe', 'Notion', 'Figma', 'Framer'] as partner}
				<div class="h-20 bg-gray-50 rounded-lg flex items-center justify-center grayscale opacity-60 hover:opacity-100 hover:grayscale-0 transition-all duration-300">
					<span class="font-semibold text-gray-700">{partner}</span>
				</div>
			{/each}
		</div>
	</section>

    <!-- Examples Section -->
    <section class="bg-white px-6 md:px-12 lg:px-24 py-12 md:py-24" id="examples">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 md:mb-24">
            <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-gray-900">Real interfaces, actually shipped</h2>
            <p class="text-gray-600 mt-4 md:mt-0 max-w-md">
                These aren't mockups. They're production interfaces built by founders using Dawnlabs.
            </p>
        </div>

        <div class="space-y-24 md:space-y-32">
            <!-- Project 1: Analytics Dashboard -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Analytics Dashboard</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        From idea to production in hours. A complete analytics dashboard with real-time data visualization, built by a solo founder with zero design experience.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Dashboard</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Data Viz</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">SaaS</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-950 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out shadow-xl">
                        <img src="/generated/image-clean-modern-dashboard-interface-on-a-la-1765980018821-0.webp" alt="Analytics Dashboard" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>

            <!-- Project 2: Landing Page -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">SaaS Landing Page</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        A conversion-optimized landing page that understands hierarchy, spacing, and user psychology. Built in an afternoon, launched the same day.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Landing Page</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Marketing</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-100 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out shadow-xl">
                        <img src="/generated/image-sleek-saas-landing-page-displayed-on-a-d-1765980023138-1.webp" alt="SaaS Landing Page" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>

            <!-- Project 3: Mobile App -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Mobile App</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        Native-feeling mobile interfaces with proper touch targets, navigation patterns, and responsive layouts. The AI understands mobile-first design principles.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Mobile</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">iOS/Android</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">App</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-950 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out shadow-xl flex items-center justify-center">
                        <img src="/generated/image-mobile-app-interface-showing-on-a-smartp-1765980025561-2.webp" alt="Mobile App" class="h-full object-contain" />
                    </div>
                </div>
            </div>

            <!-- Project 4: Admin Panel -->
            <div class="group grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <div class="lg:col-span-4 space-y-6">
                    <h3 class="font-serif text-3xl md:text-4xl text-gray-900">Admin Panel</h3>
                    <p class="text-gray-600 text-lg leading-relaxed">
                        Complex data tables, filters, and workflows that just work. The AI reasons about information architecture and user flows, not just visual design.
                    </p>
                    <div class="flex flex-wrap gap-2 pt-2">
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Admin</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Data Tables</span>
                        <span class="px-3 py-1 bg-primary-50 text-primary-700 rounded-full text-xs font-medium">Complex UI</span>
                    </div>
                </div>
                <div class="lg:col-span-8">
                    <div class="aspect-[16/9] bg-gray-100 rounded-lg overflow-hidden relative group-hover:scale-[1.02] transition-transform duration-500 ease-out shadow-xl border border-gray-200">
                        <img src="/generated/image-person-working-at-desk-with-laptop-showi-1765980028319-3.webp" alt="Admin Panel" class="w-full h-full object-cover" />
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- How It Works Section -->
    <section class="bg-gray-50 px-6 md:px-12 lg:px-24 py-12 md:py-24" id="how-it-works">
        <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-gray-900 mb-4 max-w-3xl">How it works</h2>
        <p class="text-xl text-gray-600 mb-16 max-w-2xl">Three steps from idea to production-ready interface. No design degree required.</p>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Describe -->
            <div class="bg-white p-8 rounded-xl border border-gray-200 hover:border-primary-300 transition-all duration-300 flex flex-col h-full">
                <div class="w-12 h-12 bg-primary-100 text-primary-700 rounded-lg flex items-center justify-center font-bold text-xl mb-6">1</div>
                <h3 class="text-2xl font-semibold mb-4">Describe</h3>
                <p class="text-gray-600 leading-relaxed">
                    Tell Dawnlabs what you're building. "A dashboard for tracking customer metrics" or "A mobile app for booking appointments." That's it.
                </p>
            </div>

            <!-- Reason -->
            <div class="bg-white p-8 rounded-xl border border-gray-200 hover:border-primary-300 transition-all duration-300 flex flex-col h-full">
                <div class="w-12 h-12 bg-primary-100 text-primary-700 rounded-lg flex items-center justify-center font-bold text-xl mb-6">2</div>
                <h3 class="text-2xl font-semibold mb-4">Reason</h3>
                <p class="text-gray-600 leading-relaxed">
                    Our AI reasons about structure, hierarchy, and user intent. It understands design principles, not just patterns. It thinks like a designer, not a template engine.
                </p>
            </div>

            <!-- Ship -->
            <div class="bg-white p-8 rounded-xl border border-gray-200 hover:border-primary-300 transition-all duration-300 flex flex-col h-full">
                <div class="w-12 h-12 bg-primary-100 text-primary-700 rounded-lg flex items-center justify-center font-bold text-xl mb-6">3</div>
                <h3 class="text-2xl font-semibold mb-4">Ship</h3>
                <p class="text-gray-600 leading-relaxed">
                    Get production-ready code. Clean, semantic, accessible. Copy it into your codebase or iterate further. No cleanup, no "AI slop."
                </p>
            </div>
        </div>
    </section>

    <!-- Updates Section -->
    <section class="bg-white px-6 md:px-12 lg:px-24 py-12 md:py-24">
        <div class="flex flex-col md:flex-row justify-between items-end mb-12">
            <h2 class="font-serif text-3xl md:text-4xl text-gray-900">From the lab</h2>
            <p class="text-gray-600 mt-4 md:mt-0">Updates, insights, and examples</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Post 1 -->
            <div class="group cursor-pointer">
                <div class="aspect-square bg-gradient-to-br from-primary-500 to-primary-700 rounded-lg overflow-hidden mb-4 relative">
                     <div class="absolute inset-0 flex items-center justify-center text-white font-bold text-2xl text-center p-8">
                        <span>Why reasoning beats templates</span>
                     </div>
                </div>
                <h3 class="text-base font-medium text-gray-900 group-hover:underline">How Dawnlabs thinks about design structure, not patterns</h3>
            </div>

             <!-- Post 2 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-gray-900 rounded-lg overflow-hidden mb-4 relative">
                    <div class="absolute inset-0 flex items-center justify-center text-white p-8 flex-col">
                        <span class="text-4xl mb-4">🚀</span>
                        <span class="text-xl font-semibold text-center">Product Hunt Launch</span>
                    </div>
                </div>
                <h3 class="text-base font-medium text-gray-900 group-hover:underline">We launched on Product Hunt. Here's what we learned.</h3>
            </div>

             <!-- Post 3 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-primary-950 rounded-lg overflow-hidden mb-4 relative">
                     <div class="absolute inset-0 flex items-center justify-center text-white p-8">
                        <div class="border-2 border-primary-400 rounded-lg p-6 w-full">
                            <div class="h-2 bg-primary-400 rounded mb-3 w-3/4"></div>
                            <div class="h-2 bg-primary-400/60 rounded mb-3 w-full"></div>
                            <div class="h-2 bg-primary-400/40 rounded w-1/2"></div>
                        </div>
                     </div>
                </div>
                <h3 class="text-base font-medium text-gray-900 group-hover:underline">Case study: From zero to shipped in 3 hours</h3>
            </div>

             <!-- Post 4 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-gray-100 rounded-lg overflow-hidden mb-4 relative border-2 border-gray-200">
                    <div class="absolute inset-0 flex items-center justify-center p-8">
                        <div class="text-center">
                            <div class="text-5xl font-bold text-gray-900 mb-2">vs</div>
                            <div class="text-sm text-gray-600">v0 • Galileo • Stitch</div>
                        </div>
                    </div>
                </div>
                <h3 class="text-base font-medium text-gray-900 group-hover:underline">How Dawnlabs compares to other AI design tools</h3>
            </div>

             <!-- Post 5 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-gradient-to-br from-gray-900 to-gray-700 rounded-lg overflow-hidden mb-4 relative">
                    <div class="absolute inset-0 flex items-center justify-center p-8">
                        <div class="text-white text-center">
                            <div class="text-6xl mb-4">💡</div>
                            <div class="text-lg font-semibold">Design reasoning explained</div>
                        </div>
                    </div>
                </div>
                <h3 class="text-base font-medium text-gray-900 group-hover:underline">What does it mean for AI to "reason" about design?</h3>
            </div>

             <!-- Post 6 -->
             <div class="group cursor-pointer">
                <div class="aspect-square bg-primary-100 rounded-lg overflow-hidden mb-4 relative border-2 border-primary-200">
                     <div class="absolute inset-0 flex items-center justify-center p-8">
                        <div class="text-center">
                            <div class="text-primary-700 font-mono text-sm mb-4">&lt;Component /&gt;</div>
                            <div class="text-gray-700 text-xs">Clean, semantic, accessible</div>
                        </div>
                     </div>
                </div>
                <h3 class="text-base font-medium text-gray-900 group-hover:underline">The code Dawnlabs generates (and why it's different)</h3>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="px-6 md:px-12 lg:px-24 py-12">
        <div class="bg-gradient-to-br from-primary-950 to-gray-950 rounded-2xl p-8 md:p-16 lg:p-20 text-white">
            <h3 class="font-serif text-3xl md:text-4xl mb-4">Ready to ship faster?</h3>
            <p class="text-white/70 mb-8 max-w-md text-lg">Join product builders who are already using Dawnlabs to turn ideas into production-ready interfaces.</p>
            
            <form class="flex flex-col sm:flex-row gap-4 max-w-lg">
                <input type="email" placeholder="your@email.com" class="flex-1 bg-white/10 border border-white/20 rounded-lg px-4 py-3 text-sm placeholder:text-white/40 focus:ring-2 focus:ring-primary-500 outline-none text-white" />
                <button type="submit" class="bg-primary-500 hover:bg-primary-600 transition-colors text-white px-8 py-3 rounded-lg text-sm font-medium">
                    Get early access
                </button>
            </form>
            <p class="text-[11px] text-white/50 mt-4">Join the waitlist for early access. No spam, just updates on our progress.</p>
        </div>
    </section>

    <!-- Why Dawnlabs Section -->
    <section class="relative bg-gradient-to-b from-gray-900 via-gray-950 to-black pt-32 pb-48 px-6 md:px-12 lg:px-24 overflow-hidden">
        <div class="max-w-5xl relative z-10">
            <h2 class="font-serif text-4xl md:text-6xl lg:text-7xl text-white leading-tight mb-8">
                Design tools gave you templates. <br />
                <span class="text-white/60">We give you reasoning.</span>
            </h2>
            <p class="text-xl text-white/70 max-w-3xl mb-12">
                The $50B design tools market is built on templates and patterns. Dawnlabs is different. Our AI understands structure, hierarchy, and intent—not just what looks good, but why it works.
            </p>
            
            <div class="mt-16 flex gap-4">
                 <a href="#examples" class="inline-flex items-center justify-center px-6 py-3 bg-primary-500 text-white rounded-full text-sm font-medium hover:bg-primary-600 transition-colors duration-300">
                    See examples
                </a>
                 <a href="#how-it-works" class="inline-flex items-center justify-center px-6 py-3 border border-white/30 rounded-full text-sm font-medium text-white hover:bg-white hover:text-gray-900 transition-colors duration-300 backdrop-blur-sm">
                    How it works
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black text-gray-400 px-6 md:px-12 lg:px-24 pt-24 pb-12 relative overflow-hidden">
        <div class="relative z-10">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-12 mb-24">
                <div class="col-span-1 md:col-span-2">
                    <h3 class="text-2xl font-medium text-white mb-6">Dawnlabs</h3>
                    <p class="text-gray-400 max-w-md mb-8">
                        Transform ideas into production-ready interfaces through AI that reasons about design structure, not templates.
                    </p>
                    <a href="mailto:hello@dawnlabs.ai" class="text-primary-400 hover:text-primary-300 transition-colors inline-flex items-center">
                        hello@dawnlabs.ai <span class="ml-2">→</span>
                    </a>
                </div>
                
                <div class="space-y-6">
                    <div>
                        <h4 class="font-medium text-white mb-3">Product</h4>
                        <div class="space-y-2 text-sm">
                            <a href="#examples" class="block hover:text-white transition-colors">Examples</a>
                            <a href="#how-it-works" class="block hover:text-white transition-colors">How it works</a>
                            <a href="#" class="block hover:text-white transition-colors">Pricing</a>
                            <a href="#" class="block hover:text-white transition-colors">Documentation</a>
                        </div>
                    </div>
                    
                    <div>
                        <h4 class="font-medium text-white mb-3">Company</h4>
                        <div class="space-y-2 text-sm">
                            <a href="#" class="block hover:text-white transition-colors">About</a>
                            <a href="#" class="block hover:text-white transition-colors">Blog</a>
                            <a href="#" class="block hover:text-white transition-colors">Careers</a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="flex flex-col md:flex-row justify-between items-center border-t border-gray-800 pt-8">
                <div class="mb-4 md:mb-0">
                    <!-- Logo -->
                    <svg width="60" height="35" viewBox="0 0 116 68" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M44.6215 56.0343C46.6079 53.651 49.5502 52.2726 52.6531 52.2726H94.8018C106.35 52.2726 115.711 42.9114 115.711 31.3637V20.909C115.711 9.36134 106.35 0 94.8018 0H86.6303C83.5277 0 80.5851 1.37818 78.599 3.76179L71.8003 11.9201C69.814 14.3037 66.8716 15.6818 63.7688 15.6818H21.62C10.0722 15.6818 0.710938 25.043 0.710938 36.5909V47.0454C0.710938 58.5933 10.0722 67.9546 21.62 67.9546H29.7916C32.8942 67.9546 35.8367 66.5765 37.8229 64.1929L44.6215 56.0343ZM100.029 20.909C100.029 18.022 97.6888 15.6818 94.8018 15.6818H78.7895C75.6866 15.6818 72.7443 17.0599 70.7579 19.4435L63.9593 27.602C61.9731 29.9854 59.0306 31.3637 55.9279 31.3637H21.62C18.7331 31.3637 16.3927 33.704 16.3927 36.5909V47.0454C16.3927 49.9324 18.7331 52.2726 21.62 52.2726H37.6324C40.7352 52.2726 43.6776 50.8945 45.664 48.5109L52.4626 40.3526C54.4488 37.969 57.3913 36.5909 60.4939 36.5909H94.8018C97.6888 36.5909 100.029 34.2507 100.029 31.3637V20.909Z" fill="white"/>
                    </svg>
                </div>
                
                <div class="flex gap-6 text-sm">
                    <a href="https://twitter.com/dawnlabs" class="hover:text-white transition-colors">Twitter</a>
                    <a href="https://github.com/dawnlabs" class="hover:text-white transition-colors">GitHub</a>
                    <a href="https://linkedin.com/company/dawnlabs" class="hover:text-white transition-colors">LinkedIn</a>
                    <a href="https://producthunt.com/@dawnlabs" class="hover:text-white transition-colors">Product Hunt</a>
                </div>
            </div>

            <div class="flex flex-col md:flex-row justify-between text-xs opacity-50 mt-12 gap-4">
                <p>© 2025 Dawnlabs. All rights reserved.</p>
                <div class="flex gap-6">
                    <a href="#" class="hover:opacity-100 transition-opacity">Privacy Policy</a>
                    <a href="#" class="hover:opacity-100 transition-opacity">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>
</div>

<style>
    /* Custom utility for vertical writing mode */
    .writing-vertical-rl {
        writing-mode: vertical-rl;
    }
</style>

