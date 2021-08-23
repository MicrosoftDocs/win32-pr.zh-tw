---
description: FixTimes 方法會將指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'IAMTimelineObj：： FixTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6578b18e98c99b471097c98e9dd75de1cdce0c134635cad1fb17e32340eb1a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428418"
---
# <a name="iamtimelineobjfixtimes-method"></a>IAMTimelineObj：： FixTimes 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會將 `FixTimes` 指定的開始和停止時間四捨五入到最接近的框架界限，如父群組的畫面播放速率設定所定義。

## <a name="syntax"></a>語法


```C++
HRESULT FixTimes(
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

\_如果成功，則傳回 S OK， \_ 如果物件不是群組的一部分，則傳回 E NOTINTREE。

## <a name="remarks"></a>備註

在轉譯期間，DES 會將物件的開始和停止時間四捨五入至最接近的框架界限。 不過，DES 不會覆寫物件的時間。 如果您變更群組畫面播放速率，則永遠會從原始時間計算舍入的時間。 如需詳細資訊，請參閱[DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。

您可以使用這個方法來判斷轉譯專案中的精確開始和停止時間。 例如，您應該搜尋舍入時間，而不是物件的原始開始和停止時間。 呼叫 [**IAMTimelineObj：： GetStartStop**](iamtimelineobj-getstartstop.md) 來取得原始時間，並將這些值傳遞至 `FixTimes` 。

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

[**IAMTimelineObj 介面**](iamtimelineobj.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




