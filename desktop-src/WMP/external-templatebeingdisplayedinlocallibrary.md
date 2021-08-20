---
title: TemplateBeingDisplayedInLocalLibrary
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |TemplateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- TemplateBeingDisplayedInLocalLibrary Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8292e2527fe14ec00a2bf7169b4e2ea2ca4c8229672625712ed3ad3a10e421e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648268"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>TemplateBeingDisplayedInLocalLibrary

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**TemplateBeingDisplayedInLocalLibrary** 屬性會指出目前的 [探索] 頁面所表示的摘要是否正在顯示于 [本機程式庫] 樹狀檢視控制項中。

## <a name="syntax"></a>Syntax

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。 **TRUE** 表示摘要會顯示在 [本機程式庫] 樹狀檢視控制項中。

## <a name="remarks"></a>備註

代表動態播放清單摘要的探索頁面可以顯示一個按鈕，讓使用者在其本機文件庫中「儲存」摘要。 儲存摘要，在此內容中，表示某些中繼資料會儲存在使用者的電腦上，而且摘要會列在 [本機程式庫] 樹狀檢視中的 [ **播放清單** ] 節點底下。 [探索] 頁面上的腳本可以檢查 **templateBeingDisplayedInLocalLibrary** 屬性，以判斷使用者是否已將摘要儲存在本機程式庫中。 如果使用者已經儲存摘要，[探索] 頁面應該不會顯示 [儲存] 按鈕。

代表廣播的探索頁面應該會基於相同的理由檢查 **templateBeingDisplayedInLocalLibrary** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





