---
description: GetCountOfType 方法會抓取指定之群組及其所有子系中所包含之指定類型的物件數目。
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'IAMTimeline：： GetCountOfType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e9eb896f00752c5d9369cf494e7b1426347f82a7ebe2aac74f7822a936c2ffb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401059"
---
# <a name="iamtimelinegetcountoftype-method"></a>IAMTimeline：： GetCountOfType 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取指定之 `GetCountOfType` 群組及其所有子系中所包含之指定類型的物件數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*群組* 
</dt> <dd>

要取得計數之群組的索引編號。

</dd> <dt>

*pVal* 
</dt> <dd>

以遞迴方式接收群組中包含的指定型別及其所有虛擬追蹤的物件數目。

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

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 不正確群組編號。<br/>      |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/> |



 

## <a name="remarks"></a>備註

呼叫這個方法相當於在指定的群組上呼叫 [**IAMTimelineComp：： GetCountOfType**](iamtimelinecomp-getcountoftype.md) 。 如需詳細資訊，請參閱該方法的「備註」一節。

一般來說，應用程式不會呼叫這個方法。 它是由轉譯引擎在內部呼叫。

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

[**IAMTimeline 介面**](iamtimeline.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




