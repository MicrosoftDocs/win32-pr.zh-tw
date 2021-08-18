---
description: 在提供 Jet 錯誤時， (IDA) 和未格式化的訊息字串，抓取錯誤碼識別碼。
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: efc7332530b5b03b0c9150adb8b0e105d0e5d17eeae9bbc485fb073391de2cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749678"
---
# <a name="jeterrrawmessage-function"></a>JetErrRawMessage 函式

在提供 Jet 錯誤時， (IDA) 和未格式化的訊息字串，抓取錯誤碼識別碼。

## <a name="syntax"></a>語法


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*犯 錯* 
</dt> <dd>

與所取得資訊對應的 Jet 錯誤。

</dd> <dt>

*pIda* 
</dt> <dd>

IDA 的指標。

</dd> <dt>

*pMessage* 
</dt> <dd>

錯誤訊息的指標。

</dd> <dt>

*cbMessage* 
</dt> <dd>

錯誤訊息中的位元組數目計數。

</dd> <dt>

*pcbActual* 
</dt> <dd>

讀取的實際位元組數目的指標。

</dd> <dt>

*pCoNtextId* 
</dt> <dd>

與說明檔相關聯之內容識別碼的指標。

</dd> <dt>

*pwszHelp/file* 
</dt> <dd>

指向說明錯誤之檔案的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **JET \_ errSuccess**，否則會傳回未格式化的錯誤訊息，指出失敗的特定原因。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
