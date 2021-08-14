---
description: GetTransAtTime 方法會根據指定的界限條件，抓取最接近指定時間的轉換。
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'IAMTimelineTransable：： GetTransAtTime 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: db81cf9a91f34699765e89f917ec31a902ebd188dc61dd77a1b909d10b09788c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399205"
---
# <a name="iamtimelinetransablegettransattime-method"></a>IAMTimelineTransable：： GetTransAtTime 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetTransAtTime`方法會根據指定的界限條件，抓取最接近指定時間的轉換。

## <a name="syntax"></a>語法


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
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

開始搜尋的時間，以 100-毫微秒單位表示。

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

如果方法傳回 S \_ OK，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

[**IAMTimelineTransable 介面**](iamtimelinetransable.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




