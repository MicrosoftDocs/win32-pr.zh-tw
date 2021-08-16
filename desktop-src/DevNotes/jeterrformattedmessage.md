---
description: 抓取 (IDA) 的錯誤碼識別碼，並在提供 Jet 錯誤和延伸的錯誤資訊時，建立最後的顯示字串。
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8b0fa6eb0ac4bc29e5657d3e58d9be1c27188a0faf7c7d68281ceca239dea8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955777"
---
# <a name="jeterrformattedmessage-function"></a>JetErrFormattedMessage 函式

抓取 (IDA) 的錯誤碼識別碼，並在提供 Jet 錯誤和延伸的錯誤資訊時，建立最後的顯示字串。

## <a name="syntax"></a>語法


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
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

用來查閱和格式化可顯示錯誤訊息的 Jet 錯誤號碼。

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

所有的 Jet 錯誤資訊，包括資料庫名稱、資料表名稱和任何次要錯誤資訊。

</dd> <dt>

*pIda* 
</dt> <dd>

與特定錯誤碼相關聯之 IDA 的指標。

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

說明錯誤之檔案指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **JET \_ errSuccess**，否則會傳回格式化的錯誤訊息，指出失敗的特定原因。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
