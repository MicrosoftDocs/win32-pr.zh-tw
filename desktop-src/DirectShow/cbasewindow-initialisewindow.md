---
description: InitialiseWindow 方法會初始化視窗。
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: " (Winutil 的 CBaseWindow.InitialiseWindow 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954657"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.InitialiseWindow 方法

`InitialiseWindow`方法會初始化視窗。

## <a name="syntax"></a>語法


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

根據預設，這個方法會抓取視窗的裝置內容 (DC) 的控制碼，並建立相容的記憶體 DC。 但是，如果 [**CBaseWindow：： m \_ bDoGetDC**](cbasewindow-m-bdogetdc.md) 旗標的值為 **FALSE**，則這個方法不會取出裝置內容。 記憶體 DC 在將點陣圖 blitting 至視窗之前，很適合用來選取點陣圖。

[**CBaseWindow：:D ocreatewindow**](cbasewindow-docreatewindow.md)方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




