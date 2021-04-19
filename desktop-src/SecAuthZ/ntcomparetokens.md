---
description: 比較兩個存取權杖，並判斷它們是否相等於對 AccessCheck 函數的呼叫。
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: 'NtCompareTokens 函式 (Ntseapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977864"
---
# <a name="ntcomparetokens-function"></a>NtCompareTokens 函式

**NtCompareTokens** 函式會比較兩個 [*存取權杖*](/windows/desktop/SecGloss/a-gly)，並判斷它們是否相等於對 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)函數的呼叫。

## <a name="syntax"></a>語法


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FirstTokenHandle* \[在\]
</dt> <dd>

要比較之第一個存取權杖的控制碼。 必須開啟權杖，才能存取 **權杖 \_ 查詢** 。

</dd> <dt>

*SecondTokenHandle* \[在\]
</dt> <dd>

要比較之第二個存取權杖的控制碼。 必須開啟權杖，才能存取 **權杖 \_ 查詢** 。

</dd> <dt>

*等於* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收表示 *FirstTokenHandle* 和 *SecondTokenHandle* 參數所代表的標記是否相等的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回狀態 \_ SUCCESS。

如果函式失敗，則會傳回一個 **NTSTATUS** 錯誤碼。

## <a name="remarks"></a>備註

如果下列所有條件都成立，則會將兩個存取控制權杖視為相等：

-   每一個權杖中 (SID) 的每個 [*安全性識別*](/windows/desktop/SecGloss/s-gly) 元也會出現在另一個權杖中。
-   這兩個權杖都不受限制。
-   如果這兩個權杖都受到限制，則在一個權杖中受限制的每個 SID 也會在另一個權杖中受到限制。
-   任一個權杖中出現的每個許可權也會出現在另一個權杖中。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Ntseapi。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

