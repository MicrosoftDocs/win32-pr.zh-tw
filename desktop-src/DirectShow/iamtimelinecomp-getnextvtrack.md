---
description: GetNextVTrack 方法會在指定的虛擬追蹤之後，抓取下一個虛擬追蹤。
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'IAMTimelineComp：： GetNextVTrack 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dbeaf5d7987f1baf2b3df9804c4abd3049c38042a29f4177f83abec6855140a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401049"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>IAMTimelineComp：： GetNextVTrack 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會在 `GetNextVTrack` 指定的虛擬追蹤之後抓取下一個虛擬追蹤。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

先前虛擬追蹤的指標，或為 **Null** ，以取出組合中的第一個虛擬追蹤。

</dd> <dt>

*ppNextVirtualTrack* \[擴展\]
</dt> <dd>

以優先權的順序接收下一個虛擬追蹤的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果方法抓取虛擬追蹤，則傳回 [確定]， \_ 否則傳回 FALSE。

## <a name="remarks"></a>備註

如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

 

 




