<template>
  <VbDemo>
    <VbCard title="Default">
      <VaMessageList :model-value="stringMessage" />
    </VbCard>
    <VbCard title="Message array">
      <VaMessageList
        :limit="3"
        :model-value="stringMessages"
      />
    </VbCard>
    <VbCard title="Error">
      <VaMessageList
        color="danger"
        :model-value="stringMessages"
      />
    </VbCard>
    <VbCard title="Success">
      <VaMessageList
        color="success"
        :model-value="stringMessages"
      />
    </VbCard>

    <VbCard title="Inherit attrs">
      <VaMessageList
        style="color: blue; font-size: 20px;"
      >
        Anchor
      </VaMessageList>
    </VbCard>

    <VbCard title="Slot bind">
      <VaMessageList
        style="color: blue; font-size: 20px;"
        #default="{ ariaAttributes }"
      >
        {{ ariaAttributes }}
      </VaMessageList>
    </VbCard>
  </VbDemo>
</template>

<script>
import { VaMessageList } from './index'

export default {
  components: {
    VaMessageList,
  },
  data () {
    return {
      stringMessage: 'String message',
      stringMessages: ['Message', 'Another message', 'Long long long long long long long long long long long long long long error message'],
    }
  },
}
</script>
