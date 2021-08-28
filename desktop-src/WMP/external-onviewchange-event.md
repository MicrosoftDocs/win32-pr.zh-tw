---
title: OnViewChange 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 當 Windows Media Player 中的 view 變更時，就會發生 OnViewChange 事件。
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- External. OnViewChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c01db02ef1bfd194330483c8dd7e71eba7ed09d9b347aee4b4813f413950c65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648678"
---
# <a name="externalonviewchange-event"></a>OnViewChange 事件

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

當 Windows Media Player 中的 view 變更時，就會發生 **OnViewChange** 事件。

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>可能的值

這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。

## <a name="parameters"></a>參數

處理此事件的函式不會使用任何參數。

## <a name="remarks"></a>備註

Windows Media Player 中的觀點可能會因為下列任何原因而變更：

-   使用者會與 Windows Media Player 的使用者介面互動。
-   使用者會與探索頁面互動，而 [探索] 頁面上的腳本則會呼叫 [External. changeView](external-changeview.md)。
-   使用者會與探索頁面互動，而 [探索] 頁面上的腳本則會呼叫 [External. changeViewOnlineList](external-changeviewonlinelist.md)。

當 Windows Media Player 中的 view 變更時，播放程式會呼叫[IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)來取得下一個探索頁面的 URL，以顯示。 不過，在播放玩家顯示新的 [探索] 頁面之前，它會引發 **OnViewChange** 事件。 如果 **OnViewChange** 事件處理常式呼叫 [External. cancelNavigate](external-cancelnavigate.md)，Windows Media Player 不會顯示新的 [探索] 頁面。 相反地，它會繼續顯示目前的 [探索] 頁面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**ChangeView**](external-changeview.md)
</dt> <dt>

[**ChangeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





