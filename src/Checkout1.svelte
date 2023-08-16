<script lang="ts">
  import "@picocss/pico/css/pico.css"
  import { checkIcon, cardIcon, billetIcon, pixIcon } from './utils/icons'
</script>

<div class="main md:m-0 sm:mx-2 sm:p-2 relative">
  <div class="content mx-auto" style="max-width: 1000px;">
    <div class="w-full flex flex-col md:flex-row">
      <div class="flex flex-col md:w-full"></div>
    </div>
    <div class="w-full flex flex-col md:flex-row">
      <div class="flex flex-col md:w-7/10 checkout-colum-max checkout-mx-auto">
        <div class="p-2">
          <div class="relative">
            <div class="w-full bg-center bg-cover flex flex-wrap" style="background-color: transparent;">
              <div class="w-full p-4">
                <div class="flex w-full items-center">
                  <img
                    src="https://images.pexels.com/photos/90946/pexels-photo-90946.jpeg"
                    alt=""
                    class="relative rounded-md"
                    style="max-height: 128px; height: auto; width: auto; max-width: 128px;"
                  />
                  <div class="z-10 relative flex items-end w-9/12 ml-4">
                    <div>
                      <h3 class="font-bold" style="font-size: 24px; color: #000;">
                        Produto de Destaque
                      </h3>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="sm:p-2">
          <div id="checkoutblock" class="text-black bg-white rounded-md py-4 px-3 md:px-6 mb-4 sm:mb-0 sm:border sm:shadow w-full">
            <div class="w-full">
              <div class="pb-3 pt-2">
                <label for="fullname">
                  Nome Completo
                  <input type="text" autocomplete="off" name="fullname" placeholder="Nome Completo"/>
                </label>
              </div>
              <div class="pb-3">
                <label for="fullname">
                  Email
                  <input maxlength="524288" type="text" name="email" placeholder="Email" />
                </label>
              </div>
              <div class="pb-3">
                <label for="email_confirm">
                  Confirmar Email
                  <input maxlength="524288" type="text" name="email_confirm" placeholder="Confirmar Email" />
                </label>
              </div>
              <div class="w-full flex flex-col md:flex-row flex-wrap pb-3">
                <div class="pb-3 md:flex-1 md:pb-0">
                  <div class="md:mr-2">
                    <label for="cpf">
                      CPF
                      <input maxlength="524288" type="tel" name="cpf" data-hj-whitelist="true" placeholder="CPF" /> 
                    </label>                    
                  </div>
                </div>
                <div class="md:flex-1">
                  <div class="">
                    <label for="phone">
                      Celular com DDD
                      <input maxlength="524288" type="tel" autocomplete="tel" name="phone" placeholder="Celular com DDD" />
                    </label>
                  </div>
                </div>
              </div>
              
              <div class="flex flex-col justify-center mt-6">
                <div class="grid gap-2 sm:p-2 mb-4 w-full payment-select-3 sm-payment-select-3">
                  <a href="#.html" class="flex w-full border rounded h-12 md:h-16 relative shadow-md justify-center items-center text-sm text-blue-500 border-blue-500" style="max-width: 200px;">
                    {@html checkIcon}
                    {@html cardIcon}
                    Cartão
                  </a>
                  <a href="#.html" class="flex w-full border border-gray-300 rounded h-12 md:h-16 relative shadow-md justify-center items-center text-sm hover:border-gray-600" style="max-width: 200px;">
                    {@html billetIcon}
                    Boleto
                  </a>
                  <a href="#.html" class="flex w-full border border-gray-300 rounded h-12 md:h-16 relative shadow-md justify-center items-center text-sm hover:border-gray-600" style="max-width: 200px;">
                    {@html pixIcon}
                    Pix
                  </a>
                </div>
              </div>
              <div class="flex flex-col">
                <div class="w-full md:px-4 md:pt-3 md:pb-0 md:rounded md:border md:border-gray-400 checkout-bg">
                  <div class="flex-1">
                    <form id="card_form_1" name="card_form_1" data-private="">
                      <div>
                        <div class="w-full md:mb-3">
                          <div class="w-full mb-2 md:mb-0">
                            <div class="">
                              <label for="ccnumber">
                                Número de Cartão de Crédito
                                <input maxlength="19" type="tel" autocomplete="ccnumber" name="ccnumber_1" placeholder="0000 0000 0000 0000" />
                              </label>
                            </div>
                          </div>
                        </div>
                        <div class="flex flex-wrap w-full md:mb-3">
                          <div class="w-full md:w-55/100 mb-2 md:mb-0 flex">
                            <div class="flex w-full md:mr-2">
                              <div class="w-5/12 flex-1">
                                <div class="mr-2">
                                  <label for="ccmonth_1">
                                    Mês
                                    <input maxlength="2" type="tel" name="ccmonth_1" placeholder="Mês" />
                                  </label>
                                </div>
                              </div>
                              <div class="w-7/12 flex-1">
                                <div >
                                  <label for="ccyear_1">
                                    Ano
                                    <input maxlength="2" type="tel" name="ccyear_1" placeholder="Ano" />
                                  </label>
                                  
                                  
                                </div>
                              </div>
                            </div>
                          </div>
                          <div class="w-full md:w-45/100 mb-2 md:mb-0">
                            <div class="">
                              <label for="ccv">
                                Cód. segurança
                                <input maxlength="4" type="tel" name="ccv" placeholder="Cód. segurança" />
                              </label>                              
                            </div>
                          </div>
                        </div>
                      </div>
                      <div class="w-full md:mb-3">
                        <div class="w-full mb-2 md:mb-0">
                          <div class="css-1t5upd">
                            <label for="installments">Parcelas</label>
                            <select name="installments">
                              <option value="4">4x de R$ 5,35</option>
                              <option value="3">3x de R$ 7,03</option>
                              <option value="2">2x de R$ 10,40</option>
                              <option value="1">R$ 19,90</option>
                            </select>
                          </div>
                        </div>
                      </div>
                    </form>
                  </div>
                  
                </div>
                
                <div class="w-full">
                  <div class="w-full md:mb-2 text-sm text-gray-600 flex items-center mt-4">
                    <div class="p-2 flex justify-center items-center">
                      <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512.005 512.005" style="width: 20px; height: 20px;">
                        <path
                          fill="currentColor"
                          d="M256.003,234.672c-11.76,0-21.333,9.573-21.333,21.333c0,7.792,4.409,14.329,10.667,18.053v13.947
				c0,5.896,4.771,10.667,10.667,10.667c5.896,0,10.667-4.771,10.667-10.667v-13.947c6.258-3.724,10.667-10.262,10.667-18.053
				C277.336,244.245,267.763,234.672,256.003,234.672z"
                        ></path>
                        <path fill="currentColor" d="M256.003,149.339c-17.646,0-32,14.354-32,32v10.667h64v-10.667C288.003,163.693,273.648,149.339,256.003,149.339z"></path>
                        <path
                          fill="currentColor"
                          d="M440.888,64.609l-181.333-64c-2.292-0.813-4.812-0.813-7.104,0l-181.333,64c-4.26,1.51-7.115,5.542-7.115,10.063v128
				c0,165.646,24.563,226.188,187.198,308.188c1.51,0.76,3.156,1.146,4.802,1.146c1.646,0,3.292-0.385,4.802-1.146
				c162.635-82,187.198-142.542,187.198-308.188v-128C448.003,70.151,445.148,66.12,440.888,64.609z M352.003,320.005
				c0,11.76-9.573,21.333-21.333,21.333H181.336c-11.76,0-21.333-9.573-21.333-21.333V213.339c0-11.76,9.573-21.333,21.333-21.333
				v-10.667c0-41.167,33.5-74.667,74.667-74.667s74.667,33.5,74.667,74.667v10.667c11.76,0,21.333,9.573,21.333,21.333V320.005z"
                        ></path>
                      </svg>
                    </div>
                    <div class="text-xs">
                      Nós protegemos seus dados de pagamento usando encriptação para prover segurança no nível de bancos.
                    </div>
                  </div>
                  <div class="w-full md:mb-2 text-sm text-gray-600 flex items-center mt-4">
                    <div class="p-2 flex justify-center items-center">
                      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" style="height: 20px; width: 20px;">
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01"
                        ></path>
                      </svg>
                    </div>
                    <div class="text-xs">A cobrança aparecerá na sua fatura como: <b>MON*THI</b></div>
                  </div>
                </div>
              </div>
              <!---->
              <div class="mt-6"><!----></div>
              <div class="flex flex-wrap w-full md:mb-2 justify-center items-center mt-4">
                <a href="#.html" class="w-full button hover:opacity-75 next-button font-bold p-4 text-white text-base rounded text-center uppercase" style="background-color: rgb(70, 201, 0);">Pagar Agora</a>
              </div>
              <div class="text-xss pt-1 text-gray-500 md:text-black-shade bottom-0 text-center">
                <div class="flex justify-center items-center">
                  <a href="#.html" target="_blank">
                    <img src="https://maximizandoresultados.com/wp-content/uploads/2022/03/monetizze-logo.png" class="w-20 my-2" alt="thi"/>
                  </a>
                </div>
                
                <div>
                  <p>
                    <a target="_blank" href="https://policies.google.com/privacy" class="font-bold">Política de Privacidade</a>
                    e
                    <a target="_blank" href="https://policies.google.com/terms" class="font-bold">Termos de Serviço</a>
                  </p>
                  <div class="text-xss pt-1 text-gray-500 md:text-black-shade bottom-0 text-center">
                    *Parcelamento com acréscimo
                  </div>
                  <div class="text-xss text-gray-500 md:text-black-shade bottom-0 text-center">
                    Ao prosseguir você concorda com os
                    <a target="_blank" href="https://monetizze.com.br/termos#buying" class="font-bold">Termos de Compra</a>
                  </div>
                </div>
                <div></div>
              </div>
            </div>
            <div></div>
          </div>
        </div>
      </div>
      <!---->
    </div>
  </div>
</div>