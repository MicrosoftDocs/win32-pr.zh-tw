---
title: ShowPopup 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |ShowPopup 方法
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup 方法 Windows Media Player
- showPopup 方法 Windows Media Player、External 類別
- External class Windows Media Player，showPopup 方法
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a651add93e32c1c2eb82827a4089a338341f2506ba26d9fbb06061aa6d185d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648338"
---
# <a name="externalshowpopup-method"></a>ShowPopup 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**showPopup** 方法會指示 Windows Media Player 顯示快捷方式網頁;也就是在另一個視窗中出現的網頁。

## <a name="syntax"></a>語法


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*PopupIndex* \[在\]
</dt> <dd>

指定快顯網頁索引的 (**long**) **數目**。

</dd> <dt>

*參數* \[在\]
</dt> <dd>

Windows Media Player 附加至網頁 URL 的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

Windows Media Player 不會解讀快顯索引。 識別快顯視窗的索引是由線上商店所建立，而且只有線上商店才有意義。

下列步驟顯示 Windows Media Player 如何使用 **showPopup** 方法的參數來建立快顯視窗的 URL。

1.  探索頁面上的腳本會呼叫 **showPopup**，並傳遞 *PopupIndex* 中的整數和 *參數* 中的字串。

2.  Windows Media Player 將索引傳遞給[IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) ，以抓取要顯示之網頁的 URL。

3.  Windows Media Player 會將 *參數* 以查詢字串的形式附加至 URL。 例如，如果 **GetItemInfo** 傳回 " https://www.Proseware.com/Pages/Popup1.htm "，且 *參數* 等於 "DlgX = 800&DlgY = 400&問候語 = Hi"，Windows Media Player 會建立下列 URL：

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

您可以使用 *參數* 來指定快顯視窗的大小。 例如，如果您將 *參數* 設定為 "DlgX = 800&DlgY = 400"，快顯視窗的大小會是800圖元乘以400圖元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





