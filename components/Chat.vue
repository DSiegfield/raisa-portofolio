<template>
  <div class="mockup-window border-base-primary p-5 border-solid border-4">
    <div class="w-96">
      <div class="chat chat-end">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/user.png"
              class="bg-primary"
            />
          </div>
        </div>
        <div class="chat-header">
          User
          <time class="text-xs opacity-50">12:46</time>
        </div>
        <div class="chat-bubble">Que Ferramentas de Design Sabes?</div>
        <div class="chat-footer opacity-50">Seen at 12:46</div>
      </div>

      <div class="chat chat-start w-">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/profile.jpg"
            />
          </div>
        </div>
        <div class="chat-header">
          Raisa
          <time class="text-xs opacity-50">12:46</time>
        </div>
        <div class="chat-bubble">
          Estou a aprender e a utilizar na prática Photoshop, Illustrator e
          Adobe After Effects
        </div>
        <div class="chat-footer opacity-50">Delivered</div>
      </div>

      <div class="chat chat-end">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/user.png"
              class="bg-primary"
            />
          </div>
        </div>
        <div class="chat-header">
          User
          <time class="text-xs opacity-50">12:47</time>
        </div>
        <div class="chat-bubble">E tecnologias de Web? Conheces Alguma?</div>
        <div class="chat-footer opacity-50">Seen at 12:47</div>
      </div>

      <div class="chat chat-start w-">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/profile.jpg"
            />
          </div>
        </div>
        <div class="chat-header">
          Raisa
          <time class="text-xs opacity-50">12:47</time>
        </div>
        <div class="chat-bubble overflow-hidden">
          Estive no passado a Aprender HTLM, CSS e JS, deixa-me te mostrar.
          <div class="mockup-code mt-3 over">
            <NuxtImg src="/images/htmlcssjs.png" class="w-14 h-16 mx-auto" />
            <pre data-prefix="1"><code>npm i HTML | CSS | JS</code></pre>

            <pre data-prefix="2"><code>Learning...</code></pre>

            <pre
              data-prefix="4"
              class="bg-warning text-warning-content"
            ><code>In Progress</code></pre>
            <pre data-prefix="5"><code><------xxxx> 60%</code></pre>
          </div>
        </div>
        <div class="chat-footer opacity-50">Delivered</div>
      </div>

      <div class="chat chat-end">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/user.png"
              class="bg-primary"
            />
          </div>
        </div>
        <div class="chat-header">
          User
          <time class="text-xs opacity-50">12:47</time>
        </div>
        <div class="chat-bubble">npm -i HTLM | CSS | JS what???</div>
        <div class="chat-footer opacity-50">Seen at 12:47</div>
      </div>

      <div class="chat chat-start">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/profile.jpg"
            />
          </div>
        </div>
        <div class="chat-header">
          Raisa
          <time class="text-xs opacity-50">12:47</time>
        </div>
        <div class="chat-bubble">
          KKKKK estava a brincar, o npm é um gerenciador de pacotes para Node.JS
        </div>
        <div class="chat-footer opacity-50">Delivered</div>
      </div>

      <div class="chat chat-start w-">
        <div class="chat-image avatar">
          <div class="w-10 rounded-full">
            <NuxtImg
              alt="Tailwind CSS chat bubble component"
              src="/images/profile.jpg"
            />
          </div>
        </div>
        <div class="chat-header">
          Raisa
          <time class="text-xs opacity-50">12:48</time>
        </div>
        <div class="chat-bubble overflow-hidden">
          Este WebSite comecou assim:
          <div class="mockup-code mt-3">
            <pre
              data-prefix="1"
            ><code>npx nuxi@latest init portofolio</code></pre>
            <pre data-prefix="2"><code>Installing dependencies...</code></pre>
          </div>
        </div>
        <div class="chat-footer opacity-50">Delivered</div>
      </div>
    </div>
  </div>
</template>
