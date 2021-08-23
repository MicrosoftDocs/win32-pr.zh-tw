---
title: ADSI 的 Win32 錯誤碼
description: 標準 Win32 錯誤碼也用來傳回 ADSI 錯誤訊息。
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- ADSI 的 Win32 錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b18539e93504991f244bbba8b41b13e524ff236918145deda73788169cef368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589738"
---
# <a name="win32-error-codes-for-adsi"></a>ADSI 的 Win32 錯誤碼

標準 Win32 錯誤碼也用來傳回 ADSI 錯誤訊息。 具體而言，ADSI LDAP 提供者會將所有 LDAP 錯誤碼對應至 Win32 錯誤碼。 這些錯誤碼的 **HRESULT** 值是0x8007XXXX 格式，其中最後四個十六進位數位（XXXX）對應到適當 Win32 錯誤碼的 **DWORD** 值。 例如，ADSI 錯誤值0x80072020 會以十進位的十六進位或8224提供0x2020 的 Win32 誤差值。

若要將您應用程式傳回的 ADSI 錯誤碼 **HRESULT** 值轉換為對應的 Win32 error **DWORD** 值（如上述標頭檔中所定義），請使用下列程式。

ADSI 的大部分 Win32 錯誤碼都定義于 Winerror.h .h 或 Lmerr 中。 這些檔案中的錯誤值會列為十進位值。

**將 ADSI 錯誤碼的 **HRESULT** 值轉換為對應的 Win32 error **DWORD** 值**

1.  如果開頭為十進位值，則將 **HRESULT** 值轉換為十六進位數位，如同您可能從 Visual Basic 應用程式取得的值。
2.  捨棄0x8007 元件會產生餘數。
3.  將餘數轉換成十進位數。
4.  在 Winerror.h 中查詢小數餘數。
5.  如果在 Winerror.h 中找不到，請從小數餘數減去2100，並在 Lmerr 中查詢結果。

adsi 2.0 將 LDAP 錯誤碼對應至一組 Win32 錯誤碼，該錯誤碼與 ADSI 中用於 Windows 2000 和 DS 用戶端的錯誤碼不同。 這些差異列在：

-   [Win32 錯誤碼](win32-error-codes.md)
-   [ADSI 2.0 的 Win32 錯誤碼](win32-error-codes-for-adsi-2-0.md)

 

 




