<template>
  <slot>
    <div
      class="h-[55.8rem] bg-[#111827] flex flex-row justify-center items-center"
    >
      <div class="w-5/6 h-5/6">
        <h1 class="text-[3.5rem] py-4 px-7 font-bold text-white">
          MY <span class="text-amber-400">SKILLS</span>
        </h1>
        <p class="text-[#6B7280] w-[40rem] px-7 flex justify-center">
         I am efficient at technical skills for both hardware and software. And i am willing to learn more about the field of Information Technologies.
        </p>
        <div class="px-7 w-full h-3/4 p-4">
          <div class="w-full h-full py-4 flex items-center space-x-[10rem]">
            <div
              class="text-white bg-[#020617] px-4 py-10 w-1/4 h-5/6 rounded-xl flex items-center flex-col"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="100"
                height="100"
                viewBox="0 0 48 48"
              >
                <defs>
                  <mask id="ipTSettingComputer0">
                    <g fill="none" stroke="#fff" stroke-width="4">
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M24 6H9a3 3 0 0 0-3 3v22a3 3 0 0 0 3 3h30a3 3 0 0 0 3-3v-5m-18 8v8m-10 0h20"
                      />
                      <circle cx="37" cy="13" r="3" fill="#555" />
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M37 20v-4m0-6V6m-6.062 10.5l3.464-2m5.196-3l3.464-2m-12.124 0l3.464 2m5.196 3l3.464 2"
                      />
                    </g>
                  </mask>
                </defs>
                <path
                  fill="#FFD54F"
                  d="M0 0h48v48H0z"
                  mask="url(#ipTSettingComputer0)"
                />
              </svg>
              <h1 class="py-10 text-[1.8rem] font-bold text-center">
                Hardware <span class="text-amber-300">Troubleshooting</span>
              </h1>
              <p class="px-5 text-center">
                Efficient in diagnosing and resolving technical issues to keep systems running smoothly. 
              </p>
            </div>
            <div
              class="text-white bg-[#020617] px-4 py-10 w-1/4 h-5/6 rounded-xl flex items-center flex-col"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="100"
                height="100"
                viewBox="0 0 48 48"
              >
                <g
                  fill="none"
                  stroke="#FFD54F"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="4"
                >
                  <path
                    d="M21 6H9a3 3 0 0 0-3 3v22a3 3 0 0 0 3 3h30a3 3 0 0 0 3-3V21M24 34v8"
                  />
                  <path d="m32 6l-4 4l4 4m6-8l4 4l-4 4M14 42h20" />
                </g>
              </svg>
              <h1 class="py-10 text-[1.8rem] font-bold">
                Web <span class="text-amber-300">Developer</span>
              </h1>
              <p class="px-5 text-center">
                 Efficient on developing websites that are highly functional and user-friendly. Utilizing the latest web technologies and best practices.
              </p>
            </div>
            <div
              class="text-white bg-[#020617] px-4 py-10 w-1/4 h-5/6 rounded-xl flex items-center flex-col"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="100"
                height="100"
                viewBox="0 0 24 24"
              >
                <path
                  fill="#FFD54F"
                  d="M3 17.25V21h3.75L17.81 9.93l-3.75-3.75zm19.61 1.11l-4.25 4.25l-5.2-5.2l1.77-1.77l1 1l2.47-2.48l1.42 1.42L18.36 17l1.06 1l1.42-1.4zm-16-7.53L1.39 5.64l4.25-4.25L7.4 3.16L4.93 5.64L6 6.7l2.46-2.48l1.42 1.42l-1.42 1.41l1 1zM20.71 7c.39-.39.39-1 0-1.41l-2.34-2.3c-.37-.39-1.02-.39-1.41 0l-1.84 1.83l3.75 3.75z"
                />
              </svg>
              <h1 class="py-10 text-[1.8rem] font-bold">
                Web <span class="text-amber-300">Designing</span>
              </h1>
              <p class="px-5 text-center">
                Efficient in designing websites that prioritize user experience and functionality.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </slot>
</template>
    
    