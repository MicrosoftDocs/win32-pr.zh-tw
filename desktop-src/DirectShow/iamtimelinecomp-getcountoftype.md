---
description: GetCountOfType 方法會以遞迴方式抓取此組合中所包含之指定型別的物件數目及其所有虛擬追蹤。
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'IAMTimelineComp：： GetCountOfType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b0504a7adb41a0d6a45714090a39aeefda9a3ef53b2d834540f600ec3ef871a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756408"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>IAMTimelineComp：： GetCountOfType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`GetCountOfType`方法會以遞迴方式抓取此組合中所包含之指定型別的物件數目及其所有虛擬追蹤。

## <a name="syntax"></a>語法


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* 
</dt> <dd>

以遞迴方式接收此組合中所包含之指定類型的物件數目及其所有虛擬追蹤。

</dd> <dt>

*pValWithComps* 
</dt> <dd>

接收在 *pVal* 中傳回的計數加上所搜尋的組合數目（包含此項）。

</dd> <dt>

*MajorType* 
</dt> <dd>

[**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md)列舉類型的成員，指定要計算的物件類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，否則傳回 E \_ 指標。

## <a name="remarks"></a>備註

一般來說，應用程式不會呼叫這個方法。 它是由轉譯引擎所呼叫。

如果您計算組合，在 *pVal* 中傳回的值為零，而在 *pValWithComps* 中傳回的值是組合的數目。 *\* PValWithComps* 的值包含您用來呼叫方法的組合。 例如，如果您在空的組合上呼叫這個方法，則 *\* pValWithComps* 等於1。

群組不能位於組合內，因此您無法使用這個方法來計算群組。  (傳回的計數一律為零。 ) 若要計算群組，請呼叫 [**IAMTimeline：： GetGroupCount**](iamtimeline-getgroupcount.md) 方法。

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

[**IAMTimelineComp 介面**](iamtimelinecomp.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




