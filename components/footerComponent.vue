<template>
  <div :id="'footerWrapper'">
    <img :id="'titleSvg'" src="/titles/trefort.svg" alt="Trefort">
    <div :id="'container'">
      <div :class="'externalLinks'">
        <a href="https://taszi.hu/" target="_blank">Iskola weboldala <img src="/svg/arrow-up-right.svg" alt="Nyil"></a>
        <a href="https://e-sport-talent.org/" target="_blank">E-Sport weboldal <img src="/svg/arrow-up-right.svg"
            alt="Nyil"></a>
      </div>
      <div :class="'socialLinks'">
        <a :class="'customLinks'" href="https://www.instagram.com/trefortdok/" target="_blank">
          <img src="/svg/instagram.svg" alt="Instagram" />
          trefortdok
        </a>
        <a :class="'customLinks'" href="https://www.facebook.com/bszctrefort" target="_blank">
          <img src="/svg/facebook-f.svg" alt="Facebook" />
          bszc_trefort
        </a>
        <a :class="'customLinks'" href="https://www.tiktok.com/@bszc_trefort" target="_blank">
          <img src="/svg/tiktok.svg" alt="Tiktok" />
          bszc_trefort
        </a>
      </div>
      <div :class="'timetableLinks'">
        <a :class="'a__timetableLinks'" href="https://taszi.edupage.org/timetable/" target="_blank">Hivatalos órarend
          <img src="/svg/arrow-up-right2.svg" alt="Nyil"></a>
        <a :class="'a__timetableLinks'" href="https://taszi.edupage.org/substitution/" target="_blank">Helyettesítés
          <img src="/svg/arrow-up-right2.svg" alt="Nyil"></a>
      </div>
      <div :class="'schoolAddress'">
        <a :class="'darkPurple'" href="https://maps.app.goo.gl/Pf5A9wK5vziyRPSy5" target="_blank"><u>5600 Békéscsaba,
            Puskin tér 1.</u></a>
        <br />
        <span>Békéscsabai Szakképzési Centrum
          Trefort Ágoston Technikum, Szakképző Iskola és Kollégium</span>
      </div>
    </div>
    <div :id="'footerCopyright'">
      <img src="/svg/opes-logo.svg" alt="Opes Design">
      <div :id="'footerCopyrightInner'">
        Designed by <a href="https://opes.hu/" target="_blank"><span :class="'mainPurple'">Opes </span>
          <img src="/svg/arrow-up-right.svg" alt="Nyil">
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
:root {
  --clr-main-purple: #451DE3;
  --clr-dark-purple: #1E004B;
  --clr-secondary-purple: #6D5E84;
  --clr-gray-text: #8F8F8F;
  --clr-bg-color: #F7F8FD;
}

a {
  color: var(--clr-main-purple);
}

#footerWrapper {
  display: grid;
  justify-content: center;
  border-radius: 30px 30px 0px 0px;
  background-color: #fff;
  size: 20px;
  box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
}

#container {
  display: grid;
  align-items: center;
  justify-content: center;
  grid-template-areas: "externalLinks socialLinks timetableLinks schoolAddress";
  grid-template-columns: repeat(4, 1fr);
  width: calc(100vw - 180px);
  gap: 1rem;
  height: min-content;
  padding: 4rem 0rem;
}

#footerCopyright {
  display: flex;
  align-items: center;
  justify-content: center;
  width: max-content;
  padding-bottom: 1rem;
}

#footerCopyrightInner {
  margin-left: 1rem;
}

#titleSvg {
  width: 200px;
  transform: translateY(-50%);
}

.externalLinks {
  grid-area: externalLinks;
  display: grid;
  gap: .5rem;
}

.darkPurple {
  color: var(--clr-dark-purple)
}

.mainPurple {
  color: var(--clr-main-purple);
}

.socialLinks {
  grid-area: socialLinks;
  display: grid;
  gap: .2rem;
  grid-template-columns: repeat(2, 1fr);
  width: max-content;
  text-align: center;
}

.timetableLinks {
  grid-area: timetableLinks;
  display: grid;
  gap: .5rem;
}

.schoolAddress {
  grid-area: schoolAddress;
  display: grid;
}

.schoolAddress>span {
  color: var(--clr-gray-text);
}

.customLinks {
  border: 1px solid var(--clr-main-purple);
  padding: 10px 12px;
  border-radius: 50px;
  height: min-content;
}

.a__timetableLinks {
  color: var(--clr-secondary-purple);
}

@media only screen and (max-width: 1260px) {
  #footerWrapper {
    margin-top: 6rem;
    padding-bottom: 3rem;
  }

  #footerCopyright {
    padding-top: 1rem;
    padding-bottom: 0rem;
    margin: 0 auto;
  }

  #container {
    grid-template-columns: repeat(1, 1fr);
    grid-template-areas:
      "externalLinks"
      "timetableLinks"
      "socialLinks"
      "schoolAddress";
    gap: 2rem;
    text-align: center;
    min-height: fit-content;
    padding: 2rem 0rem;
  }

  #container {
    height: auto;
  }

  #titleSvg {
    margin: 0 auto;
  }

  .externalLinks,
  .socialLinks,
  .timetableLinks,
  .schoolAddress {
    margin: 0 auto;
    align-self: center;
  }

  .socialLinks {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>