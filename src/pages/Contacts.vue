<template>
    <Layout :form="$static.metadata.formNameJobs">
        <template v-slot:title>{{$ts('Contacts')}}</template>
        <h2>{{$ts('LLC "Multi-agent systems"')}}</h2>

        <dl>
            <dt>{{$ts('PSRN')}}</dt>
            <dd>1217800127050</dd>
            <dt>{{$ts('OKVED')}}</dt>
            <dd>62.01 – {{$ts('Primary occupation')}} – "{{$ts('Computer software development')}}"</dd>
            <dt>{{$ts('Legal and actual address')}}</dt>
            <dd>{{$ts('address')}}</dd>
            <dt>E-mail</dt>
            <dd>vm@multi-agent.io</dd>
        </dl>
    </Layout>
</template>

<static-query>
query {
  metadata {
    formNameJobs
  }
}
</static-query>