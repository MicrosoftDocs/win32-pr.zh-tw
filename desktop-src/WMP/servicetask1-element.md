---
title: ServiceTask1 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 ServiceTask1 元素代表第一個線上商店工作窗格。
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- ServiceTask1 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fc22e01329728935e2953b5be7a3a1042cee00da3a3b9756915de2aeafe9b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995408"
---
# <a name="servicetask1-element"></a>ServiceTask1 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ServiceTask1** 元素代表第一個線上商店工作窗格。

``` syntax
<ServiceTask1
    URL = "URL"
/>
```

## <a name="attributes"></a>屬性



| 詞彙                                                                                                                             | 描述                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>需要 (**URL**) <br/> | Windows Media Player 顯示之網頁的 URL。<br/> |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                       |
|-----------------|-------------------------------|
| 父元素 | **ServiceInfo**               |
| 子元素  | **ButtonText**、 **ButtonTip** |



 

## <a name="remarks"></a>備註

**ServiceTask1** 被視為參與商務工作的主要工作窗格。 它是使用者選擇購買音樂時所顯示的工作窗格。

> [!Note]  
> Windows Media Player 10 有三個工作窗格，可讓線上商店顯示其網頁。 線上商店可以選擇使用一個、兩個或三個工作窗格。 Windows Media Player 11 只有一個工作窗格（以 **ServiceTask1** 表示），使用者可以按一下 [**線上商店**] 索引標籤來加以查看。

 

線上商店工作窗格共用單一瀏覽器實例。 這表示當使用者切換離開目前的服務工作時，您不應該在網頁中撰寫預期會繼續執行的腳本程式碼。

當使用者切換工作窗格時，Windows Media Player 會儲存 URL 和會話 cookie。 當使用者切換回工作窗格時，播放玩家會還原 URL 和 cookie。 如果使用者選擇使用不同的線上商店，則會清除 URL 和會話資料。

下表詳細說明以 URL 要求傳送的參數。 其他可能存在於舊版相容性的用途。



| 名稱         | 值                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *大地 水準面*      | Windows 的地理位置識別碼。 在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。 |
| *locale*     | Windows Media Player 地區設定識別碼。                                                                                                                                     |
| *userlocale* | Windows 地區設定識別碼。 地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。        |
| *version*    | 使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。                                                                         |



 

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

 

 





