<script>
    import { converted_money, input_money, old_moneda, new_moneda} from "./data";
    export let convert;

    function invertData(){
        // let temp = $converted_money
        // $converted_money = $input_money;
        // $input_money = temp;
        // let temp_moneda = $old_moneda;
        // $old_moneda = $new_moneda;
        // $new_moneda = temp_moneda;
        $converted_money = null;
        let temp_moneda = $old_moneda;
        $old_moneda = $new_moneda;
        $new_moneda = temp_moneda;
        if ($input_money && $old_moneda && $new_moneda) {
            convert();
        }
    }
</script>

<button onclick={invertData}>Invertir</button>

<style>
    /* From Uiverse.io by sekaiking */ 
button {
  background-color: white;
  color: black;
  border-radius: 10em;
  font-size: 17px;
  font-weight: 600;
  padding: 1em 2em;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
  border: 1px solid black;
  box-shadow: 0 0 0 0 black;
}

button:hover {
  transform: translateY(-4px) translateX(-2px);
  box-shadow: 2px 5px 0 0 black;
}

button:active {
  transform: translateY(2px) translateX(1px);
  box-shadow: 0 0 0 0 black;
}
</style>