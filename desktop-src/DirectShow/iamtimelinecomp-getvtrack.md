---
description: GetVTrack 方法會依指定的優先順序抓取虛擬追蹤。
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'IAMTimelineComp：： GetVTrack 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998639"
---
# <a name="iamtimelinecompgetvtrack-method"></a>IAMTimelineComp：： GetVTrack 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會依 `GetVTrack` 指定的優先順序抓取虛擬追蹤。

## <a name="syntax"></a>語法


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppVirtualTrack* \[擴展\]
</dt> <dd>

接收虛擬軌的 [**IAMTimelineObj**](iamtimelineobj.md) 介面。

</dd> <dt>

*頻率* 
</dt> <dd>

要抓取的虛擬追蹤優先權。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值：



| 傳回碼                                                                                  | Description                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 沒有具有指定優先權的虛擬追蹤。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | **Null** 指標引數。<br/>                    |



 

## <a name="remarks"></a>備註

如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

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

[**IAMTimelineComp 介面**](iamtimelinecomp.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




