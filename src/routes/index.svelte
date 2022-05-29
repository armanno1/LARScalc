<script>
    let scores = {
        q1: 0,
        q2: 0,
        q3: 0,
        q4: 0,
        q5: 0
    }

    $: sum = Math.floor(scores.q1 + scores.q2 + scores.q3 + scores.q4 + scores.q5)
</script>

<main class="mx-auto relative py-7 mx-4">
    <div class="z-10 inline-block absolute top-0 left-3">
        <h1 class="font-serif text-2xl font-bold text-grey-800 md:text-3xl py-2 px-1 bg-white">LARS* Score Calculator</h1>
    </div>
    <div class="border border-gray-400 bg-white py-4 pt-0 rounded-2xl pb-0 sm:pb-4  overflow-hidden">
        <div class="text-sm text-center my-6 text-gray-500 px-4">Emmertsen KJ, Laurberg S. Low anterior resection syndrome score: development and validation of a symptom-based scoring system for bowel dysfunction after low anterior resection for rectal cancer. Ann Surg. 2012 May;255(5):922-8.</div>
        
        <!-- q1 -->
        <div class="flex flex-col sm:flex-row bg-slate-100 p-4 mx-[-16px] px-6 sm:px-10 border-t">
            <div class="sm:basis-2/3 p-3 sm:p-1">
                1. Do you ever have occasions where you cannot control your flatus?
                <div class="text-gray-400">Score: {scores.q1}</div>
            </div>
            <div class="sm:basis-1/3 px-3 text-center sm:p-1 sm:text-left">
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q1.1">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q1" value={0} id="q1.1" bind:group={scores.q1}>
                        No, never
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q1.2">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q1" value={4} id="q1.2" bind:group={scores.q1}>
                        Yes, less than once per week
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q1.3">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q1" value={7} id="q1.3" bind:group={scores.q1}>
                        Yes, at least once per week
                    </label>            
                </div>
            </div>
        </div>

        <!-- q2 -->
        <div class="flex flex-col sm:flex-row bg-slate-100 p-4 mx-[-16px] px-6 sm:px-10 border-t">
            <div class="sm:basis-2/3 p-3 sm:p-1">
                2. Do you ever have any accidental leakage of liquid stool? 
                <div class="text-gray-400">Score: {Math.floor(scores.q2)}</div>
            </div>
            <div class="sm:basis-1/3 px-3 text-center sm:p-1 sm:text-left">
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q2.1">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q2" value={0} id="q2.1" bind:group={scores.q2}>
                        No, never
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q2.2">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q2" value={3.1} id="q2.2" bind:group={scores.q2}>
                        Yes, less than once per week
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q2.3">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q2" value={3} id="q2.3" bind:group={scores.q2}>
                        Yes, at least once per week
                    </label>            
                </div>
            </div>
        </div>

        <!-- q3 -->
        <div class="flex flex-col sm:flex-row bg-slate-100 p-4 mx-[-16px] px-6 sm:px-10 border-t">
            <div class="sm:basis-2/3 p-3 sm:p-1">
                3. How often do you open your bowels?
                <div class="text-gray-400">Score: {scores.q3}</div>
            </div>
            <div class="sm:basis-1/3 px-3 text-center sm:p-1 sm:text-left">
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q3.1">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q3" value={4} id="q3.1" bind:group={scores.q3}>
                       >7 times per day (24 hours)
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q3.2">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q3" value={2} id="q3.2" bind:group={scores.q3}>
                        4-7 times per day
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q3.3">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q3" value={0} id="q3.3" bind:group={scores.q3}>
                        1-3 times per day
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q3.4">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q3" value={5} id="q3.4" bind:group={scores.q3}>
                        Less than once per day
                    </label>            
                </div>
            </div>
        </div>

        <!-- q4 -->
        <div class="flex flex-col sm:flex-row bg-slate-100 p-4 mx-[-16px] px-6 sm:px-10 border-t">
            <div class="sm:basis-2/3 p-3 sm:p-1">
                4. Do you ever have to open your bowels again within one hour of the last bowel opening?
                <div class="text-gray-400">Score: {scores.q4}</div>
            </div>
            <div class="sm:basis-1/3 px-3 text-center sm:p-1 sm:text-left">
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q4.1">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q4" value={0} id="q4.1" bind:group={scores.q4}>
                        No, never
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q4.2">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q4" value={9} id="q4.2" bind:group={scores.q4}>
                        Yes, less than once per week
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q4.3">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q4" value={11} id="q4.3" bind:group={scores.q4}>
                        Yes, at least once per week
                    </label>            
                </div>
            </div>
        </div>

        <!-- q5 -->
        <div class="flex flex-col sm:flex-row bg-slate-100 p-4 mx-[-16px] px-6 sm:px-10 border-t">
            <div class="sm:basis-2/3 p-3 sm:p-1">
                5. Do you ever have such a strong urge to open your bowels that you have to rush to the toilet?
                <div class="text-gray-400">Score: {scores.q5}</div>
            </div>
            <div class="sm:basis-1/3 px-3 text-center sm:p-1 sm:text-left">
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q5.1">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q5" value={0} id="q5.1" bind:group={scores.q5}>
                        No, never
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q5.2">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q5" value={11} id="q5.2" bind:group={scores.q5}>
                        Yes, less than once per week
                    </label>            
                </div>
                <div class="form-check">
                    <label class="form-check-label inline-block text-gray-800" for="q5.3">
                        <input class="form-check-input appearance-none h-4 w-4 border border-gray-300 rounded-sm bg-white checked:bg-blue-600 checked:border-blue-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer" type="radio" name="score.q5" value={16} id="q5.3" bind:group={scores.q5}>
                        Yes, at least once per week
                    </label>            
                </div>
            </div>
        </div>
        <div class="fixed sm:relative bottom-0 left-0 p-0 sm:m-[-16px] sm:mt-0">
            {#if sum < 21}
                <div class="w-screen sm:w-full bg-green-50 p-4 border-t border-green-300 text-center sm:rounded-b-2xl sm:mt-0">
                    <div class="text-3xl font-bold text-green-800">{sum}</div>
                    <div class="text-xl text-green-600">No LARS</div>
                </div>
             {:else if 20 < sum && 30 > sum}
                <div class="w-screen sm:w-full bg-orange-50 rounded-b-2xl mt-0 p-4 border-t border-orange-300 text-center">
                    <div class="text-3xl font-bold text-orange-800">{sum}</div>
                    <div class="text-xl text-orange-600">Minor LARS</div>
                </div>         
            {:else}
                <div class="w-screen sm:w-full bg-red-50 rounded-b-2xl mt-0 p-4 border-t border-red-300 text-center">
                    <div class="text-3xl font-bold text-red-800">{sum}</div>
                    <div class="text-xl text-red-600">Major LARS</div>
                </div>       
            {/if}
        </div>
    </div>
    <footer class="text-center text-gray-400 text-sm my-6">
        * Low anterior resection syndrome. <br />
        Disclaimer: This is not a replacement for, nor constitutes, clinical judgement or clinical recommendation. This is not a diagnostic application. We assume no liability or responsibility for clinical decisions, injury, death or any other event to the user or any other arising from the use of this website.
    </footer>
</main>
