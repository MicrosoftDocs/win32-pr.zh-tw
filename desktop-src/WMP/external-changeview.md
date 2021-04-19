---
title: ChangeView 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 ChangeView 方法會在 Windows Media Player 中變更視圖。
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- changeView 方法 Windows Media Player
- changeView 方法 Windows Media Player、External 類別
- External class Windows Media Player，changeView 方法
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986171"
---
# <a name="externalchangeview-method"></a>ChangeView 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**ChangeView** 方法會在 Windows Media Player 中變更視圖。

## <a name="syntax"></a>語法


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
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

**字串** ，包含要在新的視圖中顯示之特定專案的識別碼。 例如，如果 *LibraryLocationType* 是 CPGenreID，則此參數會指定要在新的視圖中顯示之類型的識別碼。 這個字串可以是空的。 請參閱＜備註＞。

</dd> <dt>

*篩選* \[在\]
</dt> <dd>

包含新視圖之篩選準則的 **字串**。 此視圖會篩選成使用者已在播放程式的 word 滾輪控制項中輸入此文字。 這個字串可以是空的。

</dd> <dt>

*ViewParams* \[在\]
</dt> <dd>

包含參數的 **字串**，Windows Media Player 可供新的 [探索] 頁面使用，該頁面會以新的視圖顯示。 Windows Media Player 不會解讀這些參數。 它們是由線上商店所建立，而且只有線上商店才有意義。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在某些情況下，將 *LibraryLocationID* 參數設定為空字串是合理的。 例如，如果您將 *LibraryLocationType* 參數設定為 AllCPAlbumIDs，則新的視圖會代表所有專輯。 沒有任何個別專輯會成為新視圖的焦點，因此不需要在 *LibraryLocationID* 參數中提供專輯識別碼。

*ViewParams* 參數提供讓探索頁面與另一個探索頁面通訊的方式。 當探索頁面上的腳本呼叫 **changeView** 時，Windows Media Player 會調整其使用者介面。 該調整會導致播放程式呼叫外掛程式的 [IWMPContentPartner：： GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) 方法，以取得新探索頁面的 URL。 原始探索頁面在 *ViewParams* 參數中傳遞的字串不會傳遞至 **GetTemplate**。 不過，新的 [探索] 頁面可以藉由呼叫 [External. viewParameters](external-viewparameters.md)來取出 *ViewParams* 字串。

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

[**LibraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**LibraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**ViewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





