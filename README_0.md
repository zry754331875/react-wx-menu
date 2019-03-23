This project was based with [WeiXin Custom Menu](https://mp.weixin.qq.com/wiki?t=resource/res_main&id=mp1421141013).

### Like this:
![avatar](https://github.com/zry754331875/react-wx-menu/blob/master/WX20190222-201542@2x.png?raw=true)

## Props:

- title
- value
- baseViewUrl:string
- baseViewUrlTitle:string
- onAddMainMenu:()=>void
- onAddSubMenu:(mainMenuIndex)=>bool
- onDelteMenu:(deleteMenuItem)=>bool
## Notes: 
    If you set the baseViewUrl and baseViewUrlTitle properties at the same time, the jump page default is supported.
## Use Antd Form
```
<Form onSubmit={this.handleSave}>
    <FormItem>
        {getFieldDecorator('data', { initialValue: data })(
        <WXMenu title={detail.principalName} baseViewUrl="http://google.com" baseViewUrlTitle="默认网站" />
        )}
    </FormItem>
    <div style={{ textAlign: 'center' }}>
        <Button type="primary" htmlType="submit">
        保存
        </Button>
    </div>
</Form>
```
### Example Value:
```
{
  "selfmenu_info": { 
       "button": [ 
           { 
               "name": "button", 
               "sub_button": { 
                   "list": [ 
                       { 
                           "type": "view", 
                           "name": "view_url", 
                           "url": "http://www.qq.com"
                       }, 
                       { 
                           "type": "news", 
                           "name": "news", 
                           "value":"KQb_w_Tiz-nSdVLoTV35Psmty8hGBulGhEdbb9SKs-o",
                       },
                       {
                           "type": "video", 
                           "name": "video", 
                           "value": "http://61.182.130.30/vweixinp.tc.qq.com/1007_114bcede9a2244eeb5ab7f76d951df5f.f10.mp4?vkey=77A42D0C2015FBB0A3653D29C571B5F4BBF1D243FBEF17F09C24FF1F2F22E30881BD350E360BC53F&sha=0&save=1"
                       }, 
                       { 
                           "type": "voice",
                           "name": "voice", 
                           "value": "nTXe3aghlQ4XYHa0AQPWiQQbFW9RVtaYTLPC1PCQx11qc9UB6CiUPFjdkeEtJicn"
                       }
                   ]
               }
           }, 
           { 
               "type": "text", 
               "name": "text", 
               "value": "This is text!"
           }, 
           { 
               "type": "img", 
               "name": "photo", 
               "value": "ax5Whs5dsoomJLEppAvftBUuH7CgXCZGFbFJifmbUjnQk_ierMHY99Y5d2Cv14RD"
           }
       ]
   }
}
```