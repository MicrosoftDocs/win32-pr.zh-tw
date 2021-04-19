---
description: 建立使用者憑證以用於 NetMeeting 會議。
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995361"
---
# <a name="nmmakecert-function"></a>NmMakeCert 函式

建立使用者憑證以用於 NetMeeting 會議。

## <a name="syntax"></a>語法


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szFirstName* 
</dt> <dd>

使用者的名字。

</dd> <dt>

*szLastName* 
</dt> <dd>

使用者的姓氏。

</dd> <dt>

*szEmailName* 
</dt> <dd>

使用者的電子郵件名稱。

</dd> <dt>

*szCity* 
</dt> <dd>

使用者的城市。

</dd> <dt>

*szCountry* 
</dt> <dd>

使用者的國家/地區。

</dd> <dt>

*dwFlags* 
</dt> <dd>

指出如何建立憑證的值。 值可以是下列任何一項。



| 值                                                                                                                                                                                                                                                            | 意義                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**NMMKCERT \_\_ \_ 僅限 F 清除**</dt> <dt>0x00000004</dt> </dl>    | 刪除舊憑證，而不建立新的憑證。 <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**NMMKCERT \_F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt> </dl>  | 刪除先前使用此函數建立的舊憑證。 <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**NMMKCERT \_F \_ 本機 \_ 電腦**</dt> <dt>0x00000002</dt> </dl> | 在本機電腦憑證存放區中建立憑證。 <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回1，如果函式失敗，則傳回-1。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 
