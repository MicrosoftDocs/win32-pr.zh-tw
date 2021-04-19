---
title: ChangeViewOnlineList 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |ChangeViewOnlineList 方法
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- changeViewOnlineList 方法 Windows Media Player
- changeViewOnlineList 方法 Windows Media Player、External 類別
- External class Windows Media Player，changeViewOnlineList 方法
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980155"
---
# <a name="externalchangeviewonlinelist-method"></a>ChangeViewOnlineList 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ChangeViewOnlineList** 方法會在 Windows Media Player 中變更視圖，以顯示線上商店動態產生的清單。

## <a name="syntax"></a>語法


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*LibraryLocationType* \[在\]
</dt> <dd>

指定新檢視類型的連結 [庫位置常數](library-location-constants.md) 。 例如，常數 CPGenreID 指定新的視圖會顯示特定的內容類型。

</dd> <dt>

*LibraryLocationID* \[在\]
</dt> <dd>

**字串** ，包含要在新的視圖中顯示之特定專案的識別碼。 例如，如果 *LibraryLocationType* 是 CPGenreID，則此參數會指定要在新的視圖中顯示之類型的識別碼。 這個字串可以是空的。

</dd> <dt>

*Params* \[在\]
</dt> <dd>

包含參數的 **字串**，這些參數會藉由呼叫 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)，Windows Media Player 傳遞到線上商店的外掛程式。 Windows Media Player 不會解讀這些參數。 它們是由線上商店所建立，而且只有線上商店才有意義。 這個字串可以是空的

</dd> <dt>

*FriendlyName* \[在\]
</dt> <dd>

**字串** ，包含要顯示為動態清單之易記名稱（Windows Media Player）。

</dd> <dt>

*ListType* \[在\]
</dt> <dd>

程式庫位置常數，指定動態產生清單中的專案類型。 例如，如果此參數的值是 CPTrackID，則動態清單將包含追蹤。

</dd> <dt>

*ViewMode* \[在\]
</dt> <dd>

**字串** ，指定 Windows Media Player 將用來顯示動態清單的模式。 呼叫端必須將此參數設定為下列其中一個值（定義于 contentpartner 中）：

ViewModeReport

ViewModeDetails

ViewModeIcon

ViewModeTile

ViewModeOrderedList

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當探索頁面上的腳本呼叫 **changeViewOnlineList** 時，Windows Media Player 會將部分參數傳遞至 [IWMPContentPartner：： GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) 和 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 方法，這些方法是由線上商店的外掛程式所執行。 下表顯示這三種方法的參數之間的對應。



| changeViewOnlineList 參數 | GetListContents 參數 | GetTemplate 參數 |
|--------------------------------|---------------------------|-----------------------|
| *LocationType*                 | *location*                | *location*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrParams*              | *bstrViewParams*      |
| *ListType*                     | *bstrListType*            | 不適用        |



 

由於上表所示的三個方法都是由線上商店所執行，因此您在使用參數時有一些彈性。 其概念是，您會提供足夠的資訊供 **GetListContents** 用來判斷應取得的清單，以及讓 **GetTemplate** 判斷接下來應顯示的探索頁面。 下列範例說明兩個可能性。

**範例1：在線上商店的目錄中的動態清單**

假設您想要讓外掛程式取得線上商店目錄中識別碼為6的動態清單內容。 假設 list 6 是一份曲目清單。 您可以進行下列呼叫，以提供外掛程式足夠的資訊。


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



請注意， *Params* 參數是空的;外掛程式在其他參數中有足夠的資訊。

**範例2：不在線上商店目錄中的動態清單**

假設您想要讓外掛程式取得不在線上商店目錄中之動態清單的內容。 或許您已決定有動態清單，其中包含特定演出者挑選的歌曲。 假設演出者在線上商店的目錄中有2個識別碼。 您可以進行下列呼叫。


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



請注意， *LocationType* 和 *LocationID* 參數不會指定清單。 相反地， *Params* 參數會指定清單。 *LocationType* 和 *LocationID* 參數會傳遞至 **IWMPContentPartner：： GetListContents**，但是在此情況下， **GetListContents** 可以忽略它們。 *LocationType* 和 *LocationID* 參數也會傳遞至 **IWMPContentPartner：： GetTemplate**，這可以用來判斷應該使用動態清單來顯示的 [探索] 頁面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartnerCallback::AddListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**位置和選取的專案**](location-and-selected-item.md)
</dt> </dl>

 

 





