<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Button from "./Button.svelte";
</script>

<Meta
  title="Button"
  component={Button}
  argTypes={{
    selected: { control: "boolean" },
    text: { control: "text"},
    index: { control: "number" },
    onClick: {action: 'onClick'},
  }}
/>

<Template let:args>
  <Button {...args} />
</Template>

<Story
  name="Primary"
  args={{ 
    selected: true, 
    text: "Button", 
    index: 0, 
    onClick: {} 
  }}
/>