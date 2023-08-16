<script lang="ts">
  import {toggleModal} from './utils/modal'
  import { checkIcon, cardIcon, billetIcon, pixIcon } from './utils/icons'
</script>

<main class="container">
  <div class="bannerHeader">
    <article class="headings">
      <h2>Banner do Produto</h2>
      <h3>Produto 1</h3>
    </article>
  </div>
  <div class="grid">
    <article style="margin: 0"></article>
    <article style="margin: 0"></article>
    <article style="margin: 0"></article>
    <article style="margin: 0"></article>
    <article style="margin: 0"></article>
  </div>
  <div class="grid">
    <div class="">
      <article class="dadosPessoais">
        <h5>Dados Pessoais</h5>
        <label for="fullname">Nome Completo</label>
        <input type="text" autocomplete="off" name="fullname" placeholder="Nome Completo"/>

        <label for="fullname">Email</label>
        <input maxlength="524288" type="text" name="email" placeholder="Email" />
      
        <label for="email_confirm">Confirmar Email</label>
        <input maxlength="524288" type="text" name="email_confirm" placeholder="Confirmar Email" />

        <label for="cpf">CPF</label>
        <input maxlength="524288" type="tel" name="cpf" data-hj-whitelist="true" placeholder="CPF" />

        <label for="phone">Celular com DDD</label>
        <input maxlength="524288" type="tel" autocomplete="tel" name="phone" placeholder="Celular com DDD" />
        
      </article>
      <article class="enderecoEntrega">
        <h5>Endereço de entrega</h5>
        <label for="cep">CEP</label>
        <input type="tel" name="cep" placeholder="00000-000" />
      </article>
    </div>
    <div class="">
      <article class="dadosPagamento">
        <h5>Dados de Pagamento</h5>
        <div class="grid">
          <article style="margin-top: 0;">
            {@html cardIcon}
          </article>
          <article style="margin-top: 0;">
            {@html pixIcon}
          </article>
          <article style="margin-top: 0;">
            {@html billetIcon}
          </article>
        </div>
        <label for="ccnumber">Número de Cartão de Crédito</label>
        <input maxlength="19" type="tel" name="ccnumber_1" placeholder="0000 0000 0000 0000" />
        <div class="grid">
          <div class="grid">
            <div class="">
              <label for="ccmonth_1">Mês</label>
              <input maxlength="2" type="tel" name="ccmonth_1" placeholder="Mês" />
            </div>
            <div class="">
              <label for="ccyear_1">Ano</label>
              <input maxlength="2" type="tel" name="ccyear_1" placeholder="Ano" />
            </div>
          </div>
          <div class="">
            <label for="ccv">Cód. segurança</label>
            <input maxlength="4" type="tel" name="ccv" placeholder="Cód. segurança" />
          </div>
        </div>

        <label for="ccname">Nome do Titular</label>
        <input type="text" name="ccname" placeholder="Nome do Titular" />

        <label for="installments">Parcelas</label>
        <select name="installments">
          <option value="4">4x de R$ 5,35</option>
          <option value="3">3x de R$ 7,03</option>
          <option value="2">2x de R$ 10,40</option>
          <option value="1">R$ 19,90</option>
        </select>

        <button style="background-color: #5ABB4F;"><b>Comprar</b></button>
        <small class="text-center">
          <span>Processado por</span>
          <img src="https://maximizandoresultados.com/wp-content/uploads/2022/03/monetizze-logo.png" width="77px" alt="thi"/>
        </small>
      </article>
    </div>
  </div>
</main>
