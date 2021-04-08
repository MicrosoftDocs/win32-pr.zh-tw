---
title: HelpButton 屬性
description: 代表 [說明] 按鈕的容器。
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- HelpButton 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686106"
---
# <a name="ribbonhelpbutton-property"></a>HelpButton 屬性

代表 [說明] [按鈕](windowsribbon-controls-helpbutton.md)的容器。

## <a name="usage"></a>使用方式

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                           | 描述                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [**HelpButton**](windowsribbon-element-helpbutton.md)<br/> | 最多可能發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                   |
|-----------------------------------------------------------|
| [**功能區**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。

## <a name="examples"></a>範例

下列範例將示範執行功能區說明按鈕所需的基本標記。

這段程式碼會顯示 **HelpButton** 命令宣告。


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



這段程式碼會顯示 **HelpButton** 控制項宣告。


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





