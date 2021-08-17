---
description: GetNextSrcEx 方法會在指定的來源之後，抓取下一個來源。
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'IAMTimelineTrack：： GetNextSrcEx 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 438fcdbf4f95406994f5bf0cc63ebf5b5f600a9908419b63c4ceace65dfa9659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952797"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>IAMTimelineTrack：： GetNextSrcEx 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會在 `GetNextSrcEx` 指定的來源之後，抓取下一個來源。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLast* 
</dt> <dd>

先前來源物件的指標，或為 **Null** ，以抓取曲目中的第一個來源。

</dd> <dt>

*ppNext* \[擴展\]
</dt> <dd>

接收下一個來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法會抓取來源，則傳回 [確定]， \_ 否則傳回 FALSE。

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

[**IAMTimelineTrack 介面**](iamtimelinetrack.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




