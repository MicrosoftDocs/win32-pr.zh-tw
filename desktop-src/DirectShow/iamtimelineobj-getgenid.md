---
description: GetGenID 方法會抓取物件所產生的識別碼。 識別碼是保留的數位;應用程式不應使用它。
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'IAMTimelineObj：： GetGenID 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c48e13167e947404d0975d9f2b3695faef2e284625a287360996b4d07226bb84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400736"
---
# <a name="iamtimelineobjgetgenid-method"></a>IAMTimelineObj：： GetGenID 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetGenID` 物件所產生的識別碼。 識別碼是保留的數位;應用程式不應使用它。

## <a name="syntax"></a>語法


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* 
</dt> <dd>

接收產生的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

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

 

 




