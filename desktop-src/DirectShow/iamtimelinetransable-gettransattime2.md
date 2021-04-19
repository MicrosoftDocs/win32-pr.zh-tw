---
description: GetTransAtTime2 方法會根據指定的界限條件，抓取最接近指定時間的轉換。 這個方法相當於 IAMTimelineTransable：： GetTransAtTime，但會接受 REFTIME 參數。
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'IAMTimelineTransable：： GetTransAtTime2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998641"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>IAMTimelineTransable：： GetTransAtTime2 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetTransAtTime2`方法會根據指定的界限條件，抓取最接近指定時間的轉換。 這個方法相當於 [**IAMTimelineTransable：： GetTransAtTime**](iamtimelinetransable-gettransattime.md)，但會接受 [**REFTIME**](reftime.md) 參數。

## <a name="syntax"></a>語法


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppObj* \[擴展\]
</dt> <dd>

接收轉換 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> <dt>

*Time* 
</dt> <dd>

開始搜尋的時間（以秒為單位）。

</dd> <dt>

*SearchDirection* 
</dt> <dd>

[**DEXTERF \_ TRACK \_ 搜尋 \_ 旗標**](dexterf-track-search-flags.md)列舉類型的成員，可指定搜尋的界限條件。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | 找不到轉換。<br/>   |
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 找到轉換。<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。<br/>          |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/> |



 

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

[**IAMTimelineTransable 介面**](iamtimelinetransable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




