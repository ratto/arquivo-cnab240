<template>
    <b-form @submit="onSubmit" @reset="onReset">
        <b-row>
            <b-col cols="4">
                <fieldset>
                    <legend>Controle</legend>
                    <b-row>
                        <b-col>
                            <b-form-group
                                id="input-group-controle-banco"
                                label="Banco"
                                label-for="input-controle-banco">
                                <b-form-input
                                    id="input-controle-banco"
                                    v-model="form.controle.banco"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-controle-lote"
                                label="Lote"
                                label-for="input-controle-lote">
                                <b-form-input
                                    id="input-controle-lote"
                                    v-model="form.controle.lote"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-controle-registro"
                                label="Registro"
                                label-for="input-controle-registro">
                                <b-form-input
                                    id="input-controle-registro"
                                    v-model="form.controle.registro"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                    </b-row>
                </fieldset>
            </b-col>
            <b-col>
                <fieldset>
                    <legend>Serviço</legend>
                    <b-row>
                        <b-col>
                            <b-form-group
                                id="input-group-servico-registro"
                                label="Número do Registro"
                                label-for="input-servico-registro">
                                <b-form-input
                                    id="input-servico-registro"
                                    v-model="form.servico.numRegistro"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-servico-segmento"
                                label="Segmento"
                                label-for="input-servico-segmento">
                                <b-form-input
                                    id="input-servico-segmento"
                                    v-model="form.servico.segmento"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-servico-movimento-tipo"
                                label="Tipo de Movimento"
                                label-for="input-servico-movimento-tipo">
                                <b-form-input
                                    id="input-servico-movimento-tipo"
                                    v-model="form.servico.movimento.tipo"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-servico-movimento-codigo"
                                label="Código Movimento"
                                label-for="input-servico-movimento-codigo">
                                <b-form-input
                                    id="input-servico-movimento-codigo"
                                    v-model="form.servico.movimento.codigo"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                    </b-row>
                </fieldset>
            </b-col>
        </b-row>
        <b-row>
            <b-col>
                <fieldset>
                    <legend>Favorecido</legend>
                    <b-row>
                        <b-col cols="12">
                            <b-form-group
                                id="input-group-favorecido-nome"
                                label="Nome"
                                label-for="input-favorecido-nome">
                                <b-form-input
                                    id="input-favorecido-nome"
                                    v-model="form.favorecido.nome"
                                    type="text"
                                    placeholder="Nome do favorecido da conta">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-favorecido-camara"
                                label="Câmara"
                                label-for="input-favorecido-camara">
                                <b-form-input
                                    id="input-favorecido-camara"
                                    v-model="form.favorecido.camara"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-favorecido-banco"
                                label="Banco"
                                label-for="input-favorecido-banco">
                                <b-form-input
                                    id="input-favorecido-banco"
                                    v-model="form.favorecido.banco"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-favorecido-cc-ag-codigo"
                                label="Agência (cc)"
                                label-for="input-favorecido-cc-ag-codigo">
                                <b-form-input
                                    id="input-favorecido-cc-ag-codigo"
                                    v-model="form.favorecido.contaCorrente.agencia.codigo"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="1">
                            <b-form-group
                                id="input-group-favorecido-cc-ag-dv"
                                label="DV"
                                label-for="input-favorecido-cc-ag-dv">
                                <b-form-input
                                    id="input-favorecido-cc-ag-dv"
                                    v-model="form.favorecido.contaCorrente.agencia.dv"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col>
                            <b-form-group
                                id="input-group-favorecido-cc-conta-codigo"
                                label="Conta (cc)"
                                label-for="input-favorecido-cc-conta-codigo">
                                <b-form-input
                                    id="input-favorecido-cc-conta-codigo"
                                    v-model="form.favorecido.contaCorrente.conta.codigo"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="1">
                            <b-form-group
                                id="input-group-favorecido-cc-conta-dv"
                                label="DV"
                                label-for="input-favorecido-cc-conta-dv">
                                <b-form-input
                                    id="input-favorecido-cc-conta-dv"
                                    v-model="form.favorecido.contaCorrente.conta.dv"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                    </b-row>
                </fieldset>
            </b-col>
        </b-row>
        <b-row>
            <b-col>
                <fieldset>
                    <legend>Crédito</legend>
                    <b-row>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-seu-num"
                                label="Seu número"
                                label-for="input-credito-seu-num">
                                <b-form-input
                                    id="input-credito-seu-num"
                                    v-model="form.credito.seuNumero"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-data-pagamento"
                                label="Data do Pagamento"
                                label-for="input-credito-data-pagamento">
                                <b-form-input
                                    id="input-credito-data-pagamento"
                                    v-model="form.credito.dataPagamento"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-moeda-tipo"
                                label="Moeda"
                                label-for="input-credito-moeda-tipo">
                                <b-form-input
                                    id="input-credito-moeda-tipo"
                                    v-model="form.credito.moeda.tipo"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-moeda-quantidade"
                                label="Valor"
                                label-for="input-credito-moeda-quantidade">
                                <b-form-input
                                    id="input-credito-moeda-quantidade"
                                    v-model="form.credito.moeda.quantidade"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-valor-pagamento"
                                label="Valor do Pagamento"
                                label-for="input-credito-valor-pagamento">
                                <b-form-input
                                    id="input-credito-valor-pagamento"
                                    v-model="form.credito.valorPagamento"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-nosso-numero"
                                label="Nosso número"
                                label-for="input-credito-nosso-numero">
                                <b-form-input
                                    id="input-credito-nosso-numero"
                                    v-model="form.credito.nossoNumero"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-data-compensacao"
                                label="Data da compensação"
                                label-for="input-credito-data-compensacao">
                                <b-form-input
                                    id="input-credito-data-compensacao"
                                    v-model="form.credito.dataReal"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-credito-valor-real"
                                label="Valor Real"
                                label-for="input-credito-valor-real">
                                <b-form-input
                                    id="input-credito-valor-real"
                                    v-model="form.credito.valorReal"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                    </b-row>
                </fieldset>
            </b-col>
        </b-row>
        <b-row>
            <b-col>
                <fieldset>
                    <legend>Outros</legend>
                    <b-row>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-info-2"
                                label="Informação 2"
                                label-for="input-info-2">
                                <b-form-input
                                    id="input-info-2"
                                    v-model="form.informacao2"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-finalidade-doc"
                                label="Código finalidade (doc)"
                                label-for="input-finalidade-doc">
                                <b-form-input
                                    id="input-finalidade-doc"
                                    v-model="form.codigoFinalidade.doc"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-finalidade-ted"
                                label="Código finalidade (ted)"
                                label-for="input-finalidade-ted">
                                <b-form-input
                                    id="input-finalidade-ted"
                                    v-model="form.codigoFinalidade.ted"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="3">
                            <b-form-group
                                id="input-group-finalidade-complementar"
                                label="Código finalidade (complementar)"
                                label-for="input-finalidade-complementar">
                                <b-form-input
                                    id="input-finalidade-complementar"
                                    v-model="form.codigoFinalidade.complementar"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="2">
                            <b-form-group
                                id="input-group-cnab"
                                label="CNAB"
                                label-for="input-cnab">
                                <b-form-input
                                    id="input-cnab"
                                    v-model="form.cnab"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="5">
                            <b-form-group
                                id="input-group-aviso"
                                label="Aviso"
                                label-for="input-aviso">
                                <b-form-input
                                    id="input-aviso"
                                    v-model="form.aviso"
                                    type="number">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                        <b-col cols="5">
                            <b-form-group
                                id="input-group-ocorrencias"
                                label="Ocorrencias"
                                label-for="input-ocorrencias">
                                <b-form-input
                                    id="input-ocorrencias"
                                    v-model="form.ocorrencias"
                                    type="text">
                                </b-form-input>
                            </b-form-group>
                        </b-col>
                    </b-row>
                </fieldset>
            </b-col>
        </b-row>

        <div class="d-flex justify-content-end button-group">
            <b-button type="reset" variant="danger">Reset</b-button>
            <b-button type="submit" variant="primary">Submit</b-button>
        </div>
    </b-form>
</template>

<script>
export default {
    name: 'FormRetorno',
    data() {
        return {
            form: {
                controle: {
                    banco: null,
                    lote: null,
                    registro: 3
                },
                servico: {
                    numRegistro: null,
                    segmento: "A",
                    movimento: {
                        tipo: null,
                        codigo: null
                    }
                },
                favorecido: {
                    camara: null,
                    banco: null,
                    contaCorrente: {
                        agencia: {
                            codigo: null,
                            dv: null
                        },
                        conta: {
                            codigo: null,
                            dv: null
                        }
                    },
                    nome: ''
                },
                credito: {
                    seuNumero: '',
                    dataPagamento: null,
                    moeda: {
                        tipo: null,
                        quantidade: null
                    },
                    valorPagamento: null,
                    nossoNumero: null,
                    dataReal: null,
                    valorReal: null
                },
                informacao2: '',
                codigoFinalidade: {
                    doc: '',
                    ted: '',
                    complementar: ''
                },
                cnab: '000',
                aviso: null,
                ocorrencias: ''
            }
        }
    },
    methods: {
        onSubmit() {
            this.$emit('submit', this.form)
        },
        onReset() {
            console.log('reset')
        }
    },
    computed: {
        favorecidoCcDv(){
            return this.form.favorecido.agencia.dv + this.form.favorecido.conta.dv
        }
    }
}
</script>

<style lang="sass" scoped>

</style>