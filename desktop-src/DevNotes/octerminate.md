---
description: 關閉 [OC 管理員]。
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987042"
---
# <a name="octerminate-function"></a>OcTerminate 函式

關閉 [OC 管理員]。

## <a name="syntax"></a>語法


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OcManagerCoNtext* \[in、out\]
</dt> <dd>

在輸入時，包含 [**OcInitialize**](ocinitialize.md)所傳回的 OC 管理員內容指標。 在輸出時，接收 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
