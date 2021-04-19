---
description: SetWindowForeground 方法會將影片視窗移至前景，並選擇性地提供焦點。
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: 'CBaseControlWindow. SetWindowForeground 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997748"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>CBaseControlWindow. SetWindowForeground 方法

`SetWindowForeground`方法會將影片視窗移至前景，並選擇性地提供焦點。

## <a name="syntax"></a>語法


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*重點* 
</dt> <dd>

值，指定影片視窗是否將取得焦點。 值為1會提供視窗焦點，0則否。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                                           | Description                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | 此方法已成功。<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | 焦點不等於1或0。<br/>                                   |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | 目前的篩選未連接到完整的篩選圖形。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 




