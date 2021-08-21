---
description: 使用指定的存取權開啟執行緒物件的控制碼。
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e5f459b12d90a12b7c75aabd44d25f6fcf352aff8914e6d991471acaee400260
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079688"
---
# <a name="ntopenthread-function"></a>NtOpenThread 函式

\[您可以從 Windows 中變更或移除此函式，而不需另行通知。 請改用 [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) 函數。\]

使用指定的存取權開啟執行緒物件的控制碼。

## <a name="syntax"></a>語法


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ThreadHandle* \[擴展\]
</dt> <dd>

接收執行緒物件控制碼之變數的指標。

</dd> <dt>

*DesiredAccess* \[在\]
</dt> <dd>

[**存取 \_ 遮罩**](../secauthz/access-mask-format.md)資料類型，可為執行緒物件提供所需的存取類型。

</dd> <dt>

*ObjectAttributes* \[在\]
</dt> <dd>

[物件 \_ 屬性](https://msdn.microsoft.com/library/aa491657.aspx)結構的指標。 此結構的 **ObjectName** 成員必須是 Null。

**Windows Server 2003 和 Windows XP：** 此結構的 **ObjectName** 成員可指向物件名稱。 如果 **ObjectName** 不是 Null， *ClientId* 參數必須是 null。

</dd> <dt>

*ClientId* \[在\]
</dt> <dd>

**用戶端 \_ 識別碼** 結構的指標，識別要開啟其執行緒的執行緒。

**Windows Server 2003 和 Windows XP：****用戶端 \_ 識別碼** 結構的指標，識別要開啟其執行緒的執行緒。 此參數可以是 Null。 如果這個參數不是 Null，則 *ObjectAttributes* 參數所指向之結構的 **ObjectName** 成員必須是 null。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **NTSTATUS** 或錯誤碼。

在 WDK 中可用的 Ntstatus 標頭檔中，會列出 **ntstatus** 錯誤碼的表單和重要性，並會在 wdk 檔中說明。

## <a name="remarks"></a>備註

此函數沒有相關聯的標頭檔。 您可以在 WDK 中取得相關聯的匯入程式庫 Ntdll.dll。 您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，動態連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
