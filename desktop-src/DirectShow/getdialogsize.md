---
description: GetDialogSize 函式會捕獲資源對話方塊的大小。
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: 'GetDialogSize 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979503"
---
# <a name="getdialogsize-function"></a>GetDialogSize 函式

**GetDialogSize** 函式會捕獲資源對話方塊的大小。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*iResourceID* 
</dt> <dd>

對話方塊資源識別碼。

</dd> <dt>

*pDlgProc* 
</dt> <dd>

對話方塊程式的指標。

</dd> <dt>

*lParam* 
</dt> <dd>

傳送 \_ 至暫存對話方塊的 INITDIALOG 訊息中的值，會在建立後立即傳送至暫存對話方塊。

</dd> <dt>

*pResult* 
</dt> <dd>

**大小** 結構的指標，該結構會接收對話方塊的尺寸（以螢幕圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到對話方塊資源，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

屬性頁可以使用此函式來傳回所需的實際顯示大小。 大部分的屬性頁都是對話方塊，也就是將對話方塊範本儲存在資源檔中。 範本會使用未直接對應至螢幕圖元的對話方塊單位。 但是，屬性頁的 [**GetPageInfo**](cbasepropertypage-getpageinfo.md) 函式必須傳回實際的顯示大小（以圖元為單位）。 屬性頁可以呼叫 `GetDialogSize` 來計算顯示大小。

此函式會建立對話方塊的臨時實例。 為了避免對話方塊出現在螢幕上，資源檔中的對話方塊範本不應該有 WS \_ VISIBLE 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性頁 Helper 函數](property-page-helper-functions.md)
</dt> </dl>

 

 




