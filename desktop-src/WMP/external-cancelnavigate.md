---
title: CancelNavigate 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |CancelNavigate 方法
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- cancelNavigate 方法 Windows Media Player
- cancelNavigate 方法 Windows Media Player、External 類別
- External class Windows Media Player，cancelNavigate 方法
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152594a427282a27c493f33f648b8a889a855f40a5fb13de69b7cc342099eed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649428"
---
# <a name="externalcancelnavigate-method"></a>CancelNavigate 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**cancelNavigate** 方法會通知 Windows Media Player，即使播放程式中的視圖已經變更，也不應該顯示新的 [探索] 頁面。

## <a name="syntax"></a>語法


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當 Windows Media Player 的視圖變更時，播放程式會呼叫線上商店的外掛程式，以決定接下來要顯示的 [探索] 頁面。 不過，在某些情況下，線上商店可能會想要讓播放機繼續顯示現有的 [探索] 頁面。 下列程式會決定播放程式是否顯示新的探索頁面：

1.  使用者在播放程式的使用者介面或 [探索] 頁面上執行的動作，會要求播放程式變更其觀點。
2.  播放程式會呼叫外掛程式的 [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 方法，以決定接下來要顯示的 [探索] 頁面。 播放程式會儲存新探索頁面的 URL，但目前不會顯示新的 [探索] 頁面。
3.  Player 會引發 [OnViewChange](external-onviewchange-event.md) 事件。
4.  如果 [探索] 頁面上的 **OnViewChange** 事件處理常式呼叫 **cancelNavigate**，播放程式就不會顯示新的 [探索] 頁面 (在步驟 2) 中決定。 相反地，它會繼續顯示現有的 [探索] 頁面。 如果 **OnViewChange** 事件處理常式未呼叫 **cancelNavigate**，播放程式會顯示新的 [探索] 頁面。

例如，假設播放程式目前顯示已選取特定播放軌的專輯視圖。 也假設目前的 [探索] 頁面是代表整個專輯的頁面。 如果使用者按一下同一個專輯的不同曲目，播放程式的視圖會稍微變更，以顯示已選取新的曲目。 但不需要顯示新的 [探索] 頁面。 代表整個專輯的 [探索] 頁面仍是播放程式顯示的適當頁面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**ChangeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





