<template>
     <div class="col-lg-3 col-12 justify-content-end">
                <!--3rd box-->
                <div class="well">
                    <h3 class="text-center">Preferable Sizes</h3>
                    <!-- heading-->
                    <table class="table">
                        <tbody>
                            <tr>
                                <td><input type="checkbox" />&emsp;S</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;M</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;L</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;XL</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                            <tr>
                                <td><input type="checkbox" />&emsp;XXL</td>
                                <td align="right">
                                    <input min="0" style="width: 40px" value="1" type="number" />
                                </td>
                            </tr>
                        </tbody>
                    </table>
                    <div class="d-flex justify-content-center">
                        <button type="submit" class="btn btn-large btn-block btn-primary" name="addToTheBag" id="addToTheBag">
                            Add To Bag
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-cart4" viewBox="0 0 16 16">
                                <path d="M0 2.5A.5.5 0 0 1 .5 2H2a.5.5 0 0 1 .485.379L2.89 4H14.5a.5.5 0 0 1 .485.621l-1.5 6A.5.5 0 0 1 13 11H4a.5.5 0 0 1-.485-.379L1.61 3H.5a.5.5 0 0 1-.5-.5zM3.14 5l.5 2H5V5H3.14zM6 5v2h2V5H6zm3 0v2h2V5H9zm3 0v2h1.36l.5-2H12zm1.11 3H12v2h.61l.5-2zM11 8H9v2h2V8zM8 8H6v2h2V8zM5 8H3.89l.5 2H5V8zm0 5a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0zm9-1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm-2 1a2 2 0 1 1 4 0 2 2 0 0 1-4 0z" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>
</template>
<!----------------------------------------- --script part ----------------------------------------------------->
<script>
export default {
    name: "thirdColumn",

}
</script>
