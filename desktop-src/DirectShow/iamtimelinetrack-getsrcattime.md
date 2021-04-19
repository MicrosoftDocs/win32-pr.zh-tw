---
description: GetSrcAtTime 方法會根據指定的界限條件，抓取最接近指定時間的來源物件。
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'IAMTimelineTrack：： GetSrcAtTime 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999138"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>IAMTimelineTrack：： GetSrcAtTime 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetSrcAtTime`方法會根據指定的界限條件，抓取最接近指定時間的來源物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSrc* \[擴展\]
</dt> <dd>

接收來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> <dt>

*Time* 
</dt> <dd>

搜尋的開始時間，以 100-毫微秒單位表示。

</dd> <dt>

*SearchDirection* 
</dt> <dd>

[**DEXTERF \_ TRACK \_ 搜尋 \_ 旗標**](dexterf-track-search-flags.md)列舉類型的成員，可指定搜尋的界限條件。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                  | Description                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | 找不到來源物件。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 找到來源物件。<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。<br/>               |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/>      |



 

## <a name="remarks"></a>備註

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

 

 




