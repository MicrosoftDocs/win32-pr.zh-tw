---
description: GetNextSrc2 方法會在曲目中搜尋在指定時間或之後出現的下一個來源。 這個方法相當於 IAMTimelineTrack：： GetNextSrc，但會接受 REFTIME 值。
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'IAMTimelineTrack：： GetNextSrc2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982946"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>IAMTimelineTrack：： GetNextSrc2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetNextSrc2`方法會在曲目中搜尋在指定時間或之後出現的下一個來源。 這個方法相當於 [**IAMTimelineTrack：： GetNextSrc**](iamtimelinetrack-getnextsrc.md)，但會接受 [**REFTIME**](reftime.md) 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSrc* \[擴展\]
</dt> <dd>

接收來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> <dt>

*接腳* 
</dt> <dd>

在輸入時，包含搜尋的開始時間（以秒為單位）。 如果方法會抓取來源，則會將值設定為來源的停止時間。 如果方法未抓取來源，此值就會變成無效，而且應用程式不應使用它。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法會抓取來源，則傳回 [確定]， \_ 否則傳回 FALSE。

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

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

 

 




