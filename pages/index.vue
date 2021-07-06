<template>
  <div class="container mx-auto px-5">
    <div class="flex flex-col md:flex-row py-10 border-b-4  border-dotted">
      <div class="flex flex-col w-full md:w-1/3 justify-end">
        <div
          class="flex items-center justify-center mx-auto h-64 w-64 md:ml-0 rounded-full bg-gradient-to-r from-green-400 via-blue-500 to-red-500">
          <img class="rounded-full w-56 h-56" height="224" width="224" src="~/assets/avatar.png"
               alt="اواتار شخصی ابوالفضل نورزاد"/>
        </div>
        <div class="flex justify-between w-64 mx-auto md:ml-0 mt-8">
          <a href="http://instagram.com/abolfazlnorzad" target="_blank" rel="noreferrer">
            <InstagramSvg class="w-8 h-8 text-red-500"/>
          </a>
          <a href="http://t.me/abolfazlnourzad" target="_blank" rel="noreferrer">
            <TelegramSvg class="w-8 h-8 text-blue-500"/>
          </a>
          <a href="mailto:abolfazlnorzad78@gmail.com" target="_blank" rel="noreferrer">
            <EmailSvg class="w-8 h-8 text-green-600"/>
          </a>
        </div>
      </div>

      <div class="w-full md:w-2/3 mt-12">
        <div class="flex flex-col mx-auto w-2/3 md:w-1/2">
          <p class="text-md font-medium text-gray-700">برنامه نویس فولستک</p>
          <h2 class="text-4xl font-semibold text-gray-800 pb-4"> ابوالفضل نورزاد </h2>
          <span class="text-sm font-light text-gray-600">یه برنامه نویس مشتاق ! علاقه مند به پرسش های غیر اصولی و باگ های خطرناک.</span>
        </div>
      </div>
    </div>
    <div class="flex  flex-col space-y-8 my-10 border-b-4 pb-10 border-dotted">
      <h3 class="text-3xl text-gray-700 font-bold">مهارت ها</h3>
      <div class="">
        <p class="text-gray-900">فرانت اند</p>
        <div class="flex">
          <div class="flex flex-col w-1/5 bg-green-500 text-white hover:bg-gray-100 hover:text-green-700 mt-2 py-2 items-center border rounded">
            <VueSvg class="w-8 h-8" />
            <span>ویو</span>
          </div>
          <div class="flex w-4/5 border text-gray-800 mt-2 items-center justify-between px-2 rounded mr-2">
            <component
              v-for="(skill, index) in skills"
              :key="index"
              :is="skill.component"
              class="w-8 h-8 md:w-10 md:h-10"
              :class="skill.color"
              v-tooltip="skill.tooltip"
            />
          </div>
        </div>
      </div>

      <div class="">
        <p class="text-gray-900">بک اند</p>
        <div class="flex">
          <div class="flex flex-col w-1/5 bg-red-500 text-white hover:bg-gray-100 hover:text-red-700 mt-2 py-2 items-center border rounded">
            <VueSvg class="w-8 h-8" />
            <span>لاراول</span>
          </div>
          <div class="flex w-4/5 border text-gray-800 mt-2 items-center justify-between px-2 rounded mr-2">
            <component
              v-for="(skill, index) in backSkills"
              :key="index"
              :is="skill.component"
              class="w-8 h-8 md:w-10 md:h-10"
              :class="skill.color"
              v-tooltip="skill.tooltip"
            />
          </div>
        </div>
      </div>
      <div class="">
        <p class="text-gray-900">علاقه مند</p>
        <div class="flex">
          <div class="flex flex-col w-1/5 bg-blue-500 text-white hover:bg-gray-100 hover:text-blue-700 mt-2 py-2 items-center border rounded">
            <VueSvg class="w-8 h-8" />
            <span>ریکت</span>
          </div>
          <div class="flex w-4/5 border text-gray-800 mt-2 items-center justify-between px-2 rounded mr-2">
            <component
              v-for="(skill, index) in intrestedSkills"
              :key="index"
              :is="skill.component"
              class="w-8 h-8 md:w-10 md:h-10"
              :class="skill.color"
              v-tooltip="skill.tooltip"
            />
          </div>
        </div>
      </div>
    </div>
<!--    <div class="flex flex-col my-10 border-b-4 pb-10 border-dotted">-->
<!--      <h3 class="text-3xl text-gray-700 font-bold">پروژه ها</h3>-->
<!--      <div class="grid mx-8 md:mx-0 md:grid-cols-3 gap-6 lg:gap-16 mt-6">-->
<!--        <div class="border rounded overflow-hidden bg-white">-->
<!--          <a >-->
<!--            <img class="h-56 w-full object-cover" src="~/assets/projects/1-cart.PNG" alt="پروژه سبد خرید" />-->
<!--          </a>-->
<!--          <div class="my-3 mx-6">-->
<!--            <span class="text-3xl font-semibold text-gray-700">سبد خرید</span>-->
<!--            <div class="mt-6">-->
<!--              <span class="bg-green-600 text-white py-1 px-4 rounded-full">vue.js</span>-->
<!--              <span class="bg-green-800 text-green-100 py-1 px-4 rounded-full">vuex</span>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--        <div class="border rounded overflow-hidden bg-white">-->
<!--          <a>-->
<!--            <img class="h-56 w-full object-cover" src="~/assets/projects/2-panel.PNG" alt="پروژه پنل ادمین" />-->
<!--          </a>-->
<!--          <div class="my-3 mx-6">-->
<!--            <span class="text-3xl font-semibold text-gray-700">پنل ادمین</span>-->
<!--            <div class="mt-6">-->
<!--              <span class="bg-green-600 text-white py-1 px-4 rounded-full">vue.js</span>-->
<!--              <span class="bg-blue-800 text-blue-100 py-1 px-4 rounded-full">vuetify</span>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--        <div class="border rounded overflow-hidden bg-white">-->
<!--          <a>-->
<!--            <img class="h-56 w-full object-cover" src="~/assets/projects/3-music.PNG" alt="پروژه موزیک پلیر" />-->
<!--          </a>-->
<!--          <div class="my-3 mx-6">-->
<!--            <span class="text-3xl font-semibold text-gray-700">موزیک پلیر</span>-->
<!--            <div class="mt-6">-->
<!--              <span class="bg-green-600 text-white py-1 px-4 rounded-full">vue.js</span>-->
<!--              <span class="bg-yellow-600 text-yellow-100 py-1 px-4 rounded-full">javascript</span>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--        <div class="border rounded overflow-hidden bg-white">-->
<!--          <a  >-->
<!--            <img class="h-56 w-full object-cover" src="~/assets/projects/4-weather.PNG" alt="پروژه اب و هوا" />-->
<!--          </a>-->
<!--          <div class="my-3 mx-6">-->
<!--            <span class="text-3xl font-semibold text-gray-700">اب و هوا</span>-->
<!--            <div class="mt-6">-->
<!--              <span class="bg-green-600 text-white py-1 px-4 rounded-full">vue.js</span>-->
<!--              <span class="bg-gray-700 text-gray-100 py-1 px-4 rounded-full">rest-api</span>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--        <div class="border rounded overflow-hidden bg-white">-->
<!--          <a  target="_blank">-->
<!--            <img class="h-56 w-full object-cover" src="~/assets/projects/5-calc.PNG" alt="پروژه ماشین حساب" />-->
<!--          </a>-->
<!--          <div class="my-3 mx-6">-->
<!--            <span class="text-3xl font-semibold text-gray-700">ماشین حساب</span>-->
<!--            <div class="mt-6">-->
<!--              <span class="bg-green-600 text-white py-1 px-4 rounded-full">vue.js</span>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--        <div class="border rounded overflow-hidden bg-white">-->
<!--          <a  target="_blank">-->
<!--            <img class="h-56 w-full object-cover" src="~/assets/projects/6-template.PNG" alt="پروژه قالب فروشگاهی" />-->
<!--          </a>-->
<!--          <div class="my-3 mx-6">-->
<!--            <span class="text-3xl font-semibold text-gray-700">قالب فروشگاهی</span>-->
<!--            <div class="mt-6">-->
<!--              <span class="bg-green-600 text-white py-1 px-4 rounded-full">vue.js</span>-->
<!--              <span class="bg-blue-600 text-blue-100 py-1 px-4 rounded-full">libraries</span>-->
<!--            </div>-->
<!--          </div>-->
<!--        </div>-->
<!--      </div>-->
<!--    </div>-->
    <div class="flex flex-col my-10 border-b-4 pb-10 border-dotted">
      <h3 class="text-3xl text-gray-700 font-bold">ارتباط با من</h3>
      <div class="flex flex-col md:flex-row mt-4">
        <div class="w-full md:w-1/2">
          <form action="#">
            <div class="flex flex-col w-1/2">
              <label for="name" class="text-gray-800">نام:</label>
              <input type="text" name="name" id="name" placeholder="اسم خود را وارد کنید..." class="mt-2 px-4 py-2 rounded border-2 border-blue-300 focus:outline-none focus:border-blue-500" />
            </div>
            <div class="flex flex-col w-3/4 mt-4">
              <label for="email" class="text-gray-800">ایمیل:</label>
              <input type="email" name="email" id="email" placeholder="ایمیل خود را وارد کنید..." class="mt-2 px-4 py-2 rounded border-2 border-blue-300 focus:outline-none focus:border-blue-500" />
            </div>
            <div class="flex flex-col w-3/4 mt-4">
              <label for="description" class="text-gray-800">توضیحات:</label>
              <textarea type="text" name="description" id="description" placeholder="ایمیل خود را وارد کنید..." class="mt-2 px-4 py-2 rounded border-2 border-blue-300 focus:outline-none focus:border-blue-500" rows="8"></textarea>
            </div>
            <button type="submit" class="border-2 border-blue-300 bg-white mt-4 py-2 px-6 rounded text-blue-700 font-semibold hover:bg-blue-500 hover:text-white">
              ارسال
            </button>
          </form>
        </div>
        <div class="w-full md:w-1/2 mt-6 md:mt-0">
          <p class="text-lg text-gray-700 font-semibold">درباره من</p>
          <div class="flex mt-4 w-4/5">
            <img class="w-full h-20 rounded-lg" src="~/assets/avatar.png" alt="ابوالفضل نورزاد" />
            <p class="text-gray-800 mr-2">
              لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان گرافیک است. چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است و برای شرایط فعلی تکنولوژی مورد نیاز و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد. کتابهای زیادی در شصت و سه درصد گذشته، حال و آینده شناخت فراوا
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    skills: [
      {
        component: 'NuxtSvg',
        color: 'hover:text-green-500',
        tooltip: 'nuxt.js'
      },
      {
        component: 'VuetifySvg',
        color: 'hover:text-blue-500',
        tooltip: 'vuetify.js'
      },
      {
        component: 'BootstrapSvg',
        color: 'hover:text-purple-500',
        tooltip: 'bootstrap'
      },
      {
        component: 'BulmaSvg',
        color: 'hover:text-green-500',
        tooltip: 'bulma'
      },
      {
        component: 'TailwindSvg',
        color: 'hover:text-green-500',
        tooltip: 'tailwindcss'
      },
      {
        component: 'SassSvg',
        color: 'hover:text-pink-500',
        tooltip: 'sass'
      },
    ],
    backSkills: [
      {
        component: 'PhpSvg',
        color: 'hover:text-purple-500',
        tooltip: 'PHP'
      },
      {
        component: 'MysqlSvg',
        color: 'hover:text-indigo-500',
        tooltip: 'Mysql'
      },
      {
        component: 'ApacheSvg',
        color: 'hover:text-red-500',
        tooltip: 'Apache'
      },
      {
        component: 'DockerSvg',
        color: 'hover:text-blue-500',
        tooltip: 'Docker'
      },
      {
        component: 'RedisSvg',
        color: 'hover:text-red-500',
        tooltip: 'Redis'
      },
      {
        component: 'GitSvg',
        color: 'hover:text-yellow-500',
        tooltip: 'Git'
      },
      {
        component: 'GnuBashSvg',
        color: 'hover:text-green-500',
        tooltip: 'Bash'
      },
    ],
    intrestedSkills: [
      {
        component: 'ReduxSvg',
        color: 'hover:text-purple-500',
        tooltip: 'Redux'
      },
      {
        component: 'NextSvg',
        color: 'hover:text-black',
        tooltip: 'Next'
      },
      {
        component: 'ExpressSvg',
        color: 'hover:text-black',
        tooltip: 'Express'
      },
      {
        component: 'GraphqlSvg',
        color: 'hover:text-pink-500',
        tooltip: 'GraphQL'
      },
      {
        component: 'GatsbySvg',
        color: 'hover:text-purple-500',
        tooltip: 'Gatsby'
      },
      {
        component: 'NestSvg',
        color: 'hover:text-pink-500',
        tooltip: 'Nest'
      },
      {
        component: 'ElectronSvg',
        color: 'hover:text-indigo-500',
        tooltip: 'Electron'
      },
    ],
  })
}
</script>
