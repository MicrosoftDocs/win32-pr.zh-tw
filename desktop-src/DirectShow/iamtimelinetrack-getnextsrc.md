---
description: GetNextSrc 方法會在曲目中搜尋在指定時間或之後出現的下一個來源。
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'IAMTimelineTrack：： GetNextSrc 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000686"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>IAMTimelineTrack：： GetNextSrc 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetNextSrc`方法會在曲目中搜尋在指定時間或之後出現的下一個來源。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
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

變數的指標，其中包含搜尋的開始時間，以 100-毫微秒單位表示。 如果方法會抓取來源，則會將值設定為來源的停止時間。 如果方法未抓取來源，此值就會變成無效，而且應用程式不應使用它。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法會抓取來源，則傳回 [確定]， \_ 否則傳回 FALSE。

## <a name="remarks"></a>備註

如果由 *引線* 指定的時間介於來源的開始和停止時間之間，則該方法會抓取該來源。

如果方法傳回 S \_ OK，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

 

 




