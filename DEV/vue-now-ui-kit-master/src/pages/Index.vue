<script>
// import VueMasonryWall from "vue-masonry-wall";
import { Button, FormGroupInput } from "@/components";
// import SwiperSlider from "../components/SwiperSlider";
import InstaButton from "../components/InstaButton";
import InstaStatistic from "../components/InstaStatistic";

export default {
  name: "index",
  bodyClass: "landing-page",
  components: {
    [Button.name]: Button,
    [FormGroupInput.name]: FormGroupInput,
    InstaButton,
    InstaStatistic,
  },
  data() {
    return {
      examplePhotos: [
        { name: "img/example/example_1.jpg", src: "Пример" },
        { name: "img/example/example_2.jpg", src: "Пример" },
        { name: "img/example/example_3.jpg", src: "Пример" },
        { name: "img/example/example_4.jpg", src: "Пример" },
        { name: "img/example/example_5.jpg", src: "Пример" },
        { name: "img/example/example_6.jpg", src: "Пример" },
        { name: "img/example/example_7.jpg", src: "Пример" },
        { name: "img/example/example_8.jpg", src: "Пример" },
        { name: "img/example/example_9.jpg", src: "Пример" },
      ],
    };
  },
  methods: {},
  mounted() {
    // First we get the viewport height and we multiple it by 1% to get a value for a vh unit
    let vh = window.innerHeight * 0.01;
    // Then we set the value in the --vh custom property to the root of the document
    document.documentElement.style.setProperty("--vh", `${vh}px`);
  },
};
</script>
<template>
  <div class="">
    <div class="b1">
      <div class="main">
        <div class="b1_box">
          <div class="b1_box_1">
            <p class="b1_t1">Инста фотосет</p>
            <h1 class="h1">Фотосессии под ключ <br />для Инстаграм в Минске</h1>
          </div>
          <div class="b1_box_2">
            <div class="b1_box_2_img"></div>
            <div class="b1_box_2_text">
              <p>
                Получите бомбический <b>фотоконтент</b> для своего блога
                <b>на 2 месяца за одну съемку</b> и забудьте про проблемы с
                фотками.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="b2 border-bottom">
      <div class="main">
        <p class="zg">Для кого нужен инстафотосет?</p>
        <div class="b2_text white-background">
          <p>
            Это услуга для блогеров, экспертов и предпринимателей, которые САМИ
            ведут свой блог и продают товары/услуги через Инстаграм или ведут
            тематический блог и заинтересованы в его продвижении.
          </p>
        </div>
        <div class="b2_img">
          <img src="img/client.jpeg" alt="клиент" />
        </div>
      </div>
    </div>
    <div class="b7 border-bottom">
      <div class="main">
        <p class="zg">
          Выбирайте готовый концепт фотосета или любуйтесь своей фото-идеей в
          ленте <b>через 3 дня</b> после съемки.
        </p>
        <div class="b2_text">
          <p>
            Сделаю фото по темам ваших постов и подарю пример верстки ленты
            блога из полученного материала.
            <i class="arrs"
              ><svg
                width="16"
                height="10"
                viewBox="0 0 16 10"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M10.3164 1.31592L14.0006 5.00013L10.3164 8.68434"
                  stroke="#181818"
                  stroke-width="2"
                />
                <rect
                  y="4.26318"
                  width="13.2632"
                  height="1.47368"
                  fill="#181818"
                /></svg
            ></i>
          </p>
        </div>
      </div>
      <div class="b7_box slide">
        <div class="b7_item">
          <img src="img/example/example_1.jpg" alt="example_1" />
        </div>
        <div class="b7_item">
          <img src="img/example/example_2.jpg" alt="example_2" />
        </div>
      </div>
    </div>
    <div class="b11">
      <div class="b11_1 border-bottom">
        <div class="main">
          <p class="zg">Давайте зафиксируем вашу точку А?</p>
          <ul>
            <li>
              Сейчас у вас посредственный, неинтересный визуал в блоге, нет
              единого стиля.
              <img src="img/before_1.jpeg" alt="фото до" />
              <InstaStatistic />
            </li>
            <li>
              Фотки мало лайкают и они не способствуют новым подпискам.
              <img src="img/before_2.jpeg" alt="фото до" />
              <InstaStatistic :comments="1" :likes="12" />
            </li>

            <li>
              Нет контента для регулярного постинга, который соответствовал бы
              тематике блога или вашей личности.
              <img src="img/before_3.jpeg" alt="фото до" />
              <InstaStatistic :comments="0" :likes="3" />
            </li>
          </ul>
          <h6>ПОЧЕМУ ТАК?</h6>
          <p>
            Нет времени, нет желания и навыков для того, чтобы делать классный
            визуал для своего блога самостоятельно.
          </p>
          <p>
            Нет контента, добытого самостоятельно (или не дай бог со стоков) не
            хватает для планирования и регулярного постинга.
          </p>
        </div>
      </div>
      <div class="b11_3">
        <div class="main">
          <p class="b11_3_icon">***</p>
          <p class="b11_3_t1">А теперь давайте представим вашу точку Б?</p>
        </div>
      </div>
      <div class="b11_4">
        <img src="img/new.jpg" alt="" />
      </div>
      <div class="b11_5">
        <div class="main">
          <p class="b11_5_t1">
            Будь готов к взрывной активности <br />внутри твоего профиля
          </p>
          <InstaStatistic id="spin_counts" isRed />
          <p>
            <i
              >- “Чтобы мой профиль был красивым, с атмосферными, сюжетными,
              остроумными фото, релевантными контенту и моей личности, чтобы он
              был про меня.”</i
            >
          </p>
          <p>
            <i
              >- “Хочу достаточно контента для постинга на 2 месяца за 1 съемку,
              который будет соответствовать контент-плану или темам моих
              постов”</i
            >
          </p>
          <p>
            <i
              >- “Хочу, согласовать только дату и время - остальное не моя
              забота”</i
            >
          </p>
        </div>
      </div>
    </div>
    <div class="b8">
      <div class="b8_1">
        <div class="main">
          <p class="b3_t1">
            Давайте посмотрим как мы придем к этому результату?
          </p>
        </div>
      </div>
      <div class="b8_3">
        <div class="main">
          <p class="b8_t1">
            1. Определяем какой концепт фотосета нужен для вашего блога,
            обсуждаем темы постов и ключевые темы блога.
          </p>
        </div>
      </div>
    </div>
    <div class="b9">
      <div class="b9_2"></div>
      <div class="b9_3">
        <div class="main">
          <p class="b8_t1">
            2. Знаем, что нужно для реализации этой идеи в блоге и сколько это
            будет стоить.
          </p>
        </div>
      </div>
      <div class="b9_4"></div>
    </div>
    <div class="b10">
      <div class="b10_1"></div>
      <div class="b10_2">
        <div class="main_1">
          <p class="b10_t1">
            3. Согласовываем дату и время съемки со всеми участниками, реквизит.
          </p>
          <p class="b10_t2">
            Вы точно знаете когда, где, во сколько и за сколько случится магия.
          </p>
        </div>
      </div>
    </div>
    <div class="b8">
      <div class="b8_2"></div>
      <div class="b8_3">
        <div class="main">
          <p class="b8_t1">
            4. Во время съемки вы видите промежуточные кадры и уверены в том,
            что это совпадает с вашими ожиданиями.
          </p>
        </div>
      </div>
    </div>
    <div class="b9">
      <div class="b9_5"></div>
      <div class="b9_3">
        <div class="main">
          <p class="b8_t1">
            5. После съемки мы первично отсматриваем материал, показываем пример
            ретуши и цветокоррекции, верстаем ленту, а вы точно понимаете, что
            фотки огонь, вам нравится качество фото, у вас есть видение ленты.
          </p>
        </div>
      </div>
      <div class="b9_6"></div>
    </div>
    <div class="b10">
      <div class="b10_1"></div>
      <div class="b10_2">
        <div class="main">
          <p class="b8_t1">
            6. Через неделю вы получаете ссылку со всеми фото на google-диск, вы
            смотрите и производите окончательный расчет и радостно постите
            огненный фото в свой блог.
          </p>
          <p class="b8_t2">
            А еще рекомендуете нас всем, кто пишет: "Фото огонь🔥! Кто тебя так
            сфоткал??? 📷" И получаете скидку 🎁 20% на свою следующую
            фотосессию:)
          </p>
          <p>💣💣💣</p>
          <p class="b8_t2">
            В РЕЗУЛЬТАТЕ у вас есть бомбический фотосет и нет никаких проблем с
            фотоконтентом, а есть только растущий блог и довольные подписчики.
          </p>
        </div>
        <InstaButton />
      </div>
    </div>
    <div class="b3">
      <div class="b3_1">
        <div class="main">
          <p class="b3_t1">ПОЧЕМУ ИМЕННО ЭТО РЕШЕНИЕ?</p>
        </div>
      </div>
      <div class="b3_b2"></div>
      <div class="b3_b3">
        <div class="main">
          <ul>
            <li>
              <b>Во-первых</b>, только подготовленный заранее контент - гарантия
              регулярного постинга и того, что ваш блог будет расти и нравится
              аудитории. Блог не будет расти, если вы делаете пост 1 раз в
              месяц. А делаете вы так только по одной причине - у вас нет
              годного контента или понимания того, каким он должен быть. Мы эту
              задачку решим.
            </li>
            <li>
              <b>Во-вторых</b>: просто контента мало. Нужен контент про вас, под
              вас, на ваши темы, на темы, которые резонируют с вашей ЦА. В вашем
              блоге должны быть вы: красивы, естественны и отражены в общей
              концепции профиля.
            </li>
            <li>
              <b>В третьих</b>: Я возьму все хлопоты по организации съемки, от
              тебя только ты. Ракурсы, позы, куда смотреть, как встать, куда
              деть руки - не парьтесь! Съемку ведет профессионал, у которого за
              плечами профильное образование и опыт работы с разными моделями.
            </li>
          </ul>
          <p class="b3_t4">
            Проверенные локации, студии, опытный стилист, визажист и фотограф -
            гарантия твоих классных фотографий, растущего блога и довольных
            подписчиков.
          </p>
          <InstaButton />
        </div>
      </div>
    </div>
    <div class="b4">
      <div class="b4_1">
        <div class="main">
          <p class="b3_t1">Почему у нас точно получиться?</p>
          <p class="b3_t2">
            Каждый организационный шаг съемки продуман, подготовлен и согласован
            заранее.
          </p>
          <p class="b3_t2">
            Не было ни одной неудачной съемки, ни один клиент не сказал: мне не
            понравился результат.
          </p>
        </div>
      </div>
      <div class="b4_2"></div>
      <div class="b4_3">
        <div class="main">
          <ul>
            <li>Более 50 съемок</li>
            <li>Сотрудничество с лучшими студиями</li>
            <li>Тысячи классных фото</li>
            <li>Десятки довольных клиентов</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="b2">
      <div class="b2_top">
        <div class="main">
          <div class="b2_top_box">
            <div class="b2_top_user">
              <div class="b2_top_user_photo slide">
                <span><img src="img/user_1.jpg" alt="" /></span>
                <span><img src="img/user_2.jpg" alt="" /></span>
                <span><img src="img/user_3.jpg" alt="" /></span>
                <span><img src="img/user_4.jpg" alt="" /></span>
                <span><img src="img/user_5.jpg" alt="" /></span>
                <span><img src="img/user_6.jpg" alt="" /></span>
                <span><img src="img/user_7.jpg" alt="" /></span>
                <span><img src="img/user_8.jpg" alt="" /></span>
                <span><img src="img/user_9.jpg" alt="" /></span>
              </div>
              <p>Твой_профиль</p>
            </div>
            <p class="icon_top">
              <svg
                aria-label="Дополнительно"
                class="_8-yf5"
                fill="#262626"
                height="16"
                viewBox="0 0 48 48"
                width="16"
              >
                <circle
                  clip-rule="evenodd"
                  cx="8"
                  cy="24"
                  fill-rule="evenodd"
                  r="4.5"
                ></circle>
                <circle
                  clip-rule="evenodd"
                  cx="24"
                  cy="24"
                  fill-rule="evenodd"
                  r="4.5"
                ></circle>
                <circle
                  clip-rule="evenodd"
                  cx="40"
                  cy="24"
                  fill-rule="evenodd"
                  r="4.5"
                ></circle>
              </svg>
            </p>
          </div>
        </div>
      </div>
      <div class="b2_center">
        <div class="b2_center_item">
          <img src="img/post/user_1_post.jpeg" alt="user_1" />
        </div>
        <div class="b2_center_item">
          <img src="img/post/user_2_post.jpeg" alt="user_2" />
        </div>
        <div class="b2_center_item">
          <img
            data-src="img/post/user_3_post.jpeg"
            class="user_3"
            alt="user_3"
          />
        </div>
        <div class="b2_center_item">
          <img
            data-src="img/post/user_4_post.jpeg"
            class="user_4"
            alt="user_4"
          />
        </div>
        <div class="b2_center_item">
          <img
            data-src="img/post/user_5_post.jpeg"
            class="user_5"
            alt="user_5"
          />
        </div>
        <div class="b2_center_item">
          <img
            data-src="img/post/user_6_post.jpeg"
            class="user_6"
            alt="user_6"
          />
        </div>
        <div class="b2_center_item">
          <img
            data-src="img/post/user_7_post.jpeg"
            class="user_7"
            alt="user_7"
          />
        </div>
      </div>
      <div class="b2_footer">
        <div class="main">
          <div class="b2_footer_box_1">
            <div class="b2_footer_box_1_1">
              <i
                ><svg
                  aria-label="Нравится"
                  class="_8-yf5"
                  fill="#262626"
                  height="24"
                  viewBox="0 0 48 48"
                  width="24"
                >
                  <path
                    d="M34.6 6.1c5.7 0 10.4 5.2 10.4 11.5 0 6.8-5.9 11-11.5 16S25 41.3 24 41.9c-1.1-.7-4.7-4-9.5-8.3-5.7-5-11.5-9.2-11.5-16C3 11.3 7.7 6.1 13.4 6.1c4.2 0 6.5 2 8.1 4.3 1.9 2.6 2.2 3.9 2.5 3.9.3 0 .6-1.3 2.5-3.9 1.6-2.3 3.9-4.3 8.1-4.3m0-3c-4.5 0-7.9 1.8-10.6 5.6-2.7-3.7-6.1-5.5-10.6-5.5C6 3.1 0 9.6 0 17.6c0 7.3 5.4 12 10.6 16.5.6.5 1.3 1.1 1.9 1.7l2.3 2c4.4 3.9 6.6 5.9 7.6 6.5.5.3 1.1.5 1.6.5.6 0 1.1-.2 1.6-.5 1-.6 2.8-2.2 7.8-6.8l2-1.8c.7-.6 1.3-1.2 2-1.7C42.7 29.6 48 25 48 17.6c0-8-6-14.5-13.4-14.5z"
                  ></path></svg
              ></i>
              <i
                ><svg
                  aria-label="Комментировать"
                  class="_8-yf5"
                  fill="#262626"
                  height="24"
                  viewBox="0 0 48 48"
                  width="24"
                >
                  <path
                    clip-rule="evenodd"
                    d="M47.5 46.1l-2.8-11c1.8-3.3 2.8-7.1 2.8-11.1C47.5 11 37 .5 24 .5S.5 11 .5 24 11 47.5 24 47.5c4 0 7.8-1 11.1-2.8l11 2.8c.8.2 1.6-.6 1.4-1.4zm-3-22.1c0 4-1 7-2.6 10-.2.4-.3.9-.2 1.4l2.1 8.4-8.3-2.1c-.5-.1-1-.1-1.4.2-1.8 1-5.2 2.6-10 2.6-11.4 0-20.6-9.2-20.6-20.5S12.7 3.5 24 3.5 44.5 12.7 44.5 24z"
                    fill-rule="evenodd"
                  ></path></svg
              ></i>
              <svg
                aria-label="Поделиться публикацией"
                class="_8-yf5"
                fill="#262626"
                height="24"
                viewBox="0 0 48 48"
                width="24"
              >
                <path
                  d="M47.8 3.8c-.3-.5-.8-.8-1.3-.8h-45C.9 3.1.3 3.5.1 4S0 5.2.4 5.7l15.9 15.6 5.5 22.6c.1.6.6 1 1.2 1.1h.2c.5 0 1-.3 1.3-.7l23.2-39c.4-.4.4-1 .1-1.5zM5.2 6.1h35.5L18 18.7 5.2 6.1zm18.7 33.6l-4.4-18.4L42.4 8.6 23.9 39.7z"
                ></path>
              </svg>
            </div>
            <div class="b2_footer_box_1_2">
              <i
                ><svg
                  aria-label="Сохранить"
                  class="_8-yf5"
                  fill="#262626"
                  height="24"
                  viewBox="0 0 48 48"
                  width="24"
                >
                  <path
                    d="M43.5 48c-.4 0-.8-.2-1.1-.4L24 29 5.6 47.6c-.4.4-1.1.6-1.6.3-.6-.2-1-.8-1-1.4v-45C3 .7 3.7 0 4.5 0h39c.8 0 1.5.7 1.5 1.5v45c0 .6-.4 1.2-.9 1.4-.2.1-.4.1-.6.1zM24 26c.8 0 1.6.3 2.2.9l15.8 16V3H6v39.9l15.8-16c.6-.6 1.4-.9 2.2-.9z"
                  ></path></svg
              ></i>
            </div>
          </div>
        </div>
        <div class="b2_footer_box_2">
          <div class="main">
            <p>Понравилось <b>mrs. Smith</b> и <b>другим</b></p>
          </div>
          <InstaButton />
        </div>
      </div>
    </div>

    <div class="b5">
      <div class="b5_img"><img src="img/b5_img.jpeg" alt="How much" /></div>
      <div class="b5_box">
        <div class="main">
          <p class="b5_t1">Сколько стоит?</p>
          <p class="b5_t2">Это зависит от 4х составляющих:</p>
          <ol>
            <li>
              Концепция: Ты выбираешь готовую концепцию или предлагаешь свою
              идею съёмки
            </li>
            <li>
              Локация: Где будет проходить съемка: в студии, на улице, в
              кафе/ресторане или других местах
            </li>
            <li>Время: Количество часов съемки (Минимум 1 час)</li>
            <li>
              Сервис: Услуги парикмахера, визажиста, стилиста (если нужно)
            </li>
          </ol>
          <p class="b5_t3">
            В чат-боте тебя ждет персональный калькулятор съемки и готовые
            концепции фотосета! Давай сделаем твой профиль бомбическим?!
          </p>
          <InstaButton />
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.content-center {
  &.loaded {
    .animated-title {
      color: #ffffff;
    }
  }
  .container {
    h1 {
      &:first-of-type {
        margin-top: 10px;
      }
    }

    @media only screen and (max-width: 767px) {
      h2,
      h3 {
        padding-top: 0;
      }
      h1 {
        font-size: 3.1em;
      }
      h2 {
        font-size: 2.1em;
      }
      h3 {
        font-size: 1.4em;
      }
    }

    @media only screen and (min-width: 992px) {
      padding-top: 60px;
    }
  }
  .animated-title {
    color: transparent;

    &.first {
      transition: color 1s ease-in-out;
    }
    &.second {
      transition: color 3s ease-in-out;
    }
  }
}

.Item {
  overflow: hidden;
  border-radius: 4px;
  width: 100%;
  background: #f5f5f5;

  img {
    object-fit: cover;
    width: 100%;
    height: 100%;
    line-height: 0;
    display: block;
  }
  .Content {
    padding: 20px;
  }
}
</style>
