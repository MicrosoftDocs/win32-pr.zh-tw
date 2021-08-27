---
description: GetTimeline 方法會抓取此群組所屬的時間軸。
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'IAMTimelineGroup：： GetTimeline 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: da9064969cc026ebffb91ccbdb70bcaebab2b5d696bcb04d6c6281548721c522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086838"
---
# <a name="iamtimelinegroupgettimeline-method"></a>IAMTimelineGroup：： GetTimeline 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetTimeline` 此群組所屬的時間軸。

## <a name="syntax"></a>語法


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppTimeline* \[擴展\]
</dt> <dd>

接收時間軸的 [**IAMTimeline**](iamtimeline.md) 介面。 如果群組不是時間軸的一部分，此值會設為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果 *ppTimeline* 中傳回的值不是 **Null**，則 **IAMTimeline** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

[**IAMTimelineGroup 介面**](iamtimelinegroup.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




