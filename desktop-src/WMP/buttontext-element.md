---
title: ButtonText 項目
description: 請注意，本節將說明針對線上商店使用而設計的功能。 |ButtonText 元素
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- ButtonText 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984481"
---
# <a name="buttontext-element"></a>ButtonText 項目

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ButtonText** 元素會指定 Windows Media Player 針對工作窗格按鈕顯示的文字字串。

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                                              |
|-----------------|------------------------------------------------------|
| 父元素 | **ServiceTask1**、 **ServiceTask2**、 **ServiceTask3** |
| 子元素  | 無                                                 |



 

## <a name="remarks"></a>備註

每個 **ServiceTask1**、 **ServiceTask2** 或 **ServiceTask3** 實例都需要這個元素。

> [!Note]  
> Windows Media Player 10 有三個工作窗格，可讓線上商店顯示其網頁。 線上商店可以選擇使用一個、兩個或三個工作窗格。 Windows Media Player 11 只有一個工作窗格，使用者可以按一下 [ **線上商店** ] 索引標籤來查看。 Windows Media Player 11 會忽略 **ServiceTask2** 和 **ServiceTask3** 元素。

 

Windows Media Player 可能會裁剪按鈕文字以符合可用空間。 播放程式一律會使用 Tahoma 粗體的8點字型作為此文字。 有兩行可用來顯示按鈕文字，但播放程式不會自動將第一行的文字換行到第二行。 若要在按鈕文字中指定分行符號，請在文字字串中插入新的行 escape 序列 " \\ n"。

文字字串也會顯示在 Windows Media Player 使用者介面的 **GoTo** 功能表中。

您應使用各種不同的顯示設定來測試您的線上商店，以確保文字如預期般顯示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





