---
description: GetUserData 方法會抓取應用程式定義的持續性資料。
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'IAMTimelineObj：： GetUserData 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 49ea93d80b63b82a0fce7f5f412820534ba207fedaf27c192bd5dd5c3468400e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052707"
---
# <a name="iamtimelineobjgetuserdata-method"></a>IAMTimelineObj：： GetUserData 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetUserData` 應用程式定義的持續性資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.Pdata* 
</dt> <dd>

接收資料之緩衝區的指標。 若要判斷要配置的緩衝區大小，請將此參數設定為 **Null**。 所需的大小會在 *pSize* 中傳回。

</dd> <dt>

*pSize* 
</dt> <dd>

接收資料的大小（以位元組為單位）。

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

 

 




