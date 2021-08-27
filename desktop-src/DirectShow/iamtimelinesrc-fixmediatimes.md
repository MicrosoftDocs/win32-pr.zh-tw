---
description: FixMediaTimes 方法會將指定的時間值四捨五入到最接近的框架界限（如輸出畫面播放速率所定義）。 一般情況下，應用程式不需要呼叫此方法。
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'IAMTimelineSrc：： FixMediaTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dcace4e501a27b1f82b148533f382f5c86bafb17d9bf34343f1e43a8893672c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052398"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>IAMTimelineSrc：： FixMediaTimes 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `FixMediaTimes` 指定的時間值四捨五入到最接近的框架界限（如輸出畫面播放速率所定義）。 一般情況下，應用程式不需要呼叫此方法。

## <a name="syntax"></a>語法


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStart* 
</dt> <dd>

變數的指標，該變數包含開始時間，以 100-毫微秒單位表示。 如果呼叫成功，這個變數會設定為舍入時間。

</dd> <dt>

*pStop* 
</dt> <dd>

包含停止時間之變數的指標，以 100-毫微秒單位表示。 如果呼叫成功，這個變數會設定為舍入時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法類似于 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md) 方法，但會保留媒體時間與時間軸時間的原始比例。 只將時間四捨五入到最接近的框架界限可能會扭曲此比例。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSrc 介面**](iamtimelinesrc.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




