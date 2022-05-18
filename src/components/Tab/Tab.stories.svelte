<script>
    import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
    import Tab from "./Tab.svelte";
    
</script>
  
  <Meta
    title="Tab"
    component={Tab}
  />
  
  <Template let:args>
    <Tab {...args} />
  </Template>
  
  <Story
    name="Primary"
    args={{
    tab: [
        {
            buttonText: 'Tab 1',
            paneText: 'Texto do Tab 1'
        },
        {
            buttonText: 'Tab 2',
            paneText: 'Texto do Tab 2'
        },
        {
            buttonText: 'Tab 3',
            paneText: 'Texto do Tab 3'
        },
        {
            buttonText: 'Tab 4',
            paneText: 'Texto do Tab 4'
        }
    ]
  }}
  />
  
  