---
description: LogError 方法會記錄錯誤。 應用程式不需要呼叫此方法。 它會在內部呼叫，以回應呈現錯誤。
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'IAMErrorLog：： LogError 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993488"
---
# <a name="iamerrorloglogerror-method"></a>IAMErrorLog：： LogError 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**LogError** 方法會記錄錯誤。 應用程式不需要呼叫此方法。 它會在內部呼叫，以回應呈現錯誤。

## <a name="syntax"></a>語法


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*嚴重性* 
</dt> <dd>

保留的。 請勿使用。

</dd> <dt>

*ErrorString* 
</dt> <dd>

包含錯誤文字的字串值。

</dd> <dt>

*ErrorCode* 
</dt> <dd>

錯誤碼。

</dd> <dt>

*hresult* 
</dt> <dd>

造成錯誤的方法呼叫所傳回的 HRESULT 值。

</dd> <dt>

*pExtraInfo* \[在\]
</dt> <dd>

VARIANT 的指標，其中包含有關錯誤的任何其他資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 *hresult* 參數的值。

## <a name="remarks"></a>備註

在這個方法中，請勿釋放 *pExtraInfo* 所指向的 **變異**。 此外，此 **變數** 會在方法傳回之後變成無效，因此請勿稍後再參考。

執行此方法以儘快傳回。 請勿從這個可能會封鎖程式執行的方法內部進行函式呼叫。 例如，請勿呼叫傳送視窗訊息、封鎖事件的函式，否則可能會封鎖執行。 這樣做可能會導致電腦停止回應。

如需 DES 定義的錯誤清單，以及 *pExtraInfo* 所指向之 **變異** 的意義和資料類型，請參閱轉譯 [錯誤](rendering-errors.md)。

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

[**IAMErrorLog 介面**](iamerrorlog.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




