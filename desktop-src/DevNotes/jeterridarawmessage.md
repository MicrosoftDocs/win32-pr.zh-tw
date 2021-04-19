---
description: 當提供 (IDA) 的錯誤碼識別碼時，會抓取未格式化的訊息字串。
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997737"
---
# <a name="jeterridarawmessage-function"></a>JetErrIDARawMessage 函式

當提供 (IDA) 的錯誤碼識別碼時，會抓取未格式化的訊息字串。

## <a name="syntax"></a>語法


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*艾達* 
</dt> <dd>

對應至特定錯誤碼的數位，並向使用者顯示。

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

如果函式成功，它會傳回 **JET \_ errSuccess**，否則會傳回未格式化的訊息，指出失敗的特定原因。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
