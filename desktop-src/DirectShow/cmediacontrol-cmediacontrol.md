---
description: CMediaControl。 CMediaControl 函式-函數方法。
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: 'CMediaControl. CMediaControl (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099206"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>CMediaControl. CMediaControl 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

用於偵測之物件名稱的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。

</dd> </dl>

## <a name="remarks"></a>備註

在靜態記憶體中配置 *pName* 參數。 這個名稱會在物件的建立和刪除時，出現在偵錯工具的終端機上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaControl 類別**](cmediacontrol.md)
</dt> </dl>

 

 




