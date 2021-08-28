---
description: InsertSpace2 方法會分割存在於指定時間的任何物件，並在兩者之間插入空格。 這個方法相當於 IAMTimelineTrack：： InsertSpace，但會接受 REFTIME 的值。
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'IAMTimelineTrack：： InsertSpace2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f851e6bdccb755977210fcd67e7ce0bb6cb270ec3ff6a4f1fed4806a035a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052248"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>IAMTimelineTrack：： InsertSpace2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`InsertSpace2`方法會分割存在於指定時間的任何物件，並在兩者之間插入空格。 這個方法相當於 [**IAMTimelineTrack：： InsertSpace**](iamtimelinetrack-insertspace.md)，但會接受 [**REFTIME**](reftime.md) 的值。

## <a name="syntax"></a>語法


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rtStart* 
</dt> <dd>

建立分割的時間，以及插入的空間開始點（以秒為單位）。

</dd> <dt>

*rtEnd* 
</dt> <dd>

插入空間的結束點（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的傳回值包括下列各項：



| 傳回碼                                                                                   | 描述                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | 在指定的時間沒有任何物件。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 無效引數。<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                        |



 

## <a name="remarks"></a>備註

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

[**IAMTimelineTrack 介面**](iamtimelinetrack.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




