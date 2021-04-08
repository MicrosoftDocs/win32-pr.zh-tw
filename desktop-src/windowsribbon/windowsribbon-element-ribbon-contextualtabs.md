---
title: CoNtextualTabs 屬性
description: 表示內容索引標籤的容器。
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- CoNtextualTabs 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685666"
---
# <a name="ribboncontextualtabs-property"></a>CoNtextualTabs 屬性

表示內容索引標籤的容器。

## <a name="usage"></a>使用方式

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                       | 描述                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/> | 至少必須發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                   |
|-----------------------------------------------------------|
| [**功能區**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。

內容索引標籤適合用來顯示僅與特定應用程式內容相關的功能，例如文字編輯器中的 [影像格式設定] 索引標籤，只有在顯示影像時才會顯示。 一般而言，在特定應用程式內容發生之前，內容索引標籤不會顯示，而應用程式會通知功能區架構。

顯示時，內容索引標籤會以色彩標示，以區別它們與一般索引標籤。

## <a name="examples"></a>範例

下列範例示範 **CoNtextualTabs** 元素的基本標記。

這段程式碼會顯示 [**TabGroup**](windowsribbon-element-tabgroup.md) 命令宣告和兩個內容索引卷 [**標命令宣告**](windowsribbon-element-tab.md) 。


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



這一節的程式碼會顯示 **CoNtextualTabs** 控制項宣告與 [**TabGroup**](windowsribbon-element-tabgroup.md) ，以及兩個內容相關的 [**選項卡**](windowsribbon-element-tab.md) 控制項。


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**功能區] 索引標籤**](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





