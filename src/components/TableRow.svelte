<script>
  import { faker } from '../../node_modules/@faker-js/faker';
  const helpers = faker.helpers.contextualCard();
  console.log(helpers);

  let Person = {
    name: helpers.name,
    username: helpers.username,
    email: helpers.email,
    phone: helpers.phone,
    website: helpers.website,
    avatar: helpers.avatar,
  };
  export let number;
</script>

<div class="row">
  <div class="col col-number">{number}</div>
  <div class="col col-name">{Person.name}</div>
  <div class="col col-username">{Person.username}</div>
  <div class="col col-email">{Person.email}</div>
  <div class="col col-phone">{Person.phone}</div>
  <div class="col col-website">{Person.website}</div>
  <div class="col col-avatar">
    <img src={Person.avatar} alt="{Person.name} avatar" />
  </div>
</div>

<style>
  div {
    background-color: antiquewhite;
  }
  .row {
    padding-bottom: 10px;
    padding-top: 10px;
    display: table;
    width: 100%;
  }
  .row:hover > .col,
  .row:hover {
    background-color: rgb(199, 183, 165);
  }
  .col {
    display: inline-table;
    font-size: 10px;
    text-align: center;
    vertical-align: middle;
  }
  .col-number {
    width: 5%;
  }
  .col-name,
  .col-username,
  .col-phone,
  .col-website,
  .col-email {
    width: 15%;
  }

  .col-avatar {
    width: 18%;
  }
</style>
