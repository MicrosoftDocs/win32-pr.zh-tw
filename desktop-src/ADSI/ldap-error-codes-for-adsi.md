---
title: ADSI 的 LDAP 錯誤碼
description: 當 LDAP 伺服器產生錯誤並將錯誤傳遞給用戶端時，LDAP 用戶端就會將錯誤轉譯成字串。
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6280784d8bf9fc9c692cb38f1ca2d0e76646b1d2a3d464e516f03e7ac682fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005508"
---
# <a name="ldap-error-codes-for-adsi"></a>ADSI 的 LDAP 錯誤碼

當 LDAP 伺服器產生錯誤並將錯誤傳遞給用戶端時，LDAP 用戶端就會將錯誤轉譯成字串。

這個方法類似于 [ADSI 的 Win32 錯誤碼](win32-error-codes-for-adsi.md)。 在此範例中，用戶端錯誤碼是 WIN32 error 0x80072020。

**判斷 ADSI 的 LDAP 錯誤碼**

1.  從 WIN32 錯誤碼卸載8007。 在此範例中，其餘的十六進位值為2020。
2.  將其餘的十六進位值轉換成十進位值。 在此範例中，其餘的十六進位值2020會轉換成十進位值8224。
3.  在 Winerror.h .h 檔案中搜尋 decimal 值的定義。 在此範例中，8224L 對應至 error **error \_ DS \_ 作業 \_ 錯誤**。
4.  將首碼 **錯誤 \_ DS** 取代為 **LDAP \_**。 在此範例中，新的定義是 **LDAP \_ 作業 \_ 錯誤**。
5.  在 Winldap .h 檔案中搜尋 LDAP 錯誤定義的值。 在此範例中，Winldap 檔中的 **LDAP \_ 作業 \_ 錯誤** 值為0x01。

 

 




