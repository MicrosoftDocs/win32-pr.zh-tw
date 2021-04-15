---
description: CNG 資料保護 API 會使用下列常數。
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: 'CNG DPAPI 常數 (NCryptprotect .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468732"
---
# <a name="cng-dpapi-constants"></a>CNG DPAPI 常數

CNG 資料保護 API 會使用下列常數。

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT \_ 描述 \_ 分隔符號 \_ 和**
</dt> <dd> <dl> <dt>

L "和"
</dt> <dt>



可以用來測試和分隔符號的保護描述項字串。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ 描述 \_ 等於**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



可以用來測試等號的保護描述項字串。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT \_ 描述 \_ 分隔符號 \_ 或**
</dt> <dd> <dl> <dt>

L "或"
</dt> <dt>



可以用來測試或分隔符號的保護描述項字串。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**本機的 NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



本機保護描述項可將內容保護至登入會話、目前的使用者或本機電腦，如下列常數所識別：

-   **NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 登入**
-   **NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 使用者**
-   **NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 電腦**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SDDL**
</dt> <dd> <dl> <dt>

SDDL
</dt> <dt>



將內容保護 (安全描述項定義語言的 SDDL，) 包含安全描述項資訊的字串。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SID**
</dt> <dd> <dl> <dt>

SID
</dt> <dt>



SID 保護描述項包含群組或主體身分識別。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ WEBCREDENTIALS**
</dt> <dd> <dl> <dt>

WEBCREDENTIALS
</dt> <dt>



保護使用者的 web 帳號憑證。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 登入**
</dt> <dd> <dl> <dt>

登錄
</dt> <dt>



保護目前登入會話的內容。 登出或重新開機之後，使用者將無法再解密受保護的內容。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 電腦**
</dt> <dd> <dl> <dt>

設備
</dt> <dt>



保護本機電腦的內容。 本機電腦上的所有使用者都可以解密受保護的內容。


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT \_ 金鑰 \_ 保護 \_ 本機 \_ 使用者**
</dt> <dd> <dl> <dt>

使用者名
</dt> <dt>



保護目前使用者會話的內容。 只有本機電腦上的此使用者才能解密受保護的內容。


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS \_ 金鑰 \_ 保護 \_ 提供者**
</dt> <dd> <dl> <dt>

「Microsoft 金鑰保護提供者」
</dt> <dt>



代表 Microsoft 金鑰保護提供者，它支援下列常數所代表的格式：

-   **NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SID**
-   **本機的 NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_**
-   **NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ SDDL**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS \_ 用戶端 \_ 金鑰 \_ 保護 \_ 提供者**
</dt> <dd> <dl> <dt>

「Windows 用戶端金鑰保護提供者」
</dt> <dt>



代表只能在用戶端上使用的 Microsoft 金鑰保護提供者，並支援下列常數所代表的格式：

-   **NCRYPT \_ 金鑰 \_ 保護 \_ 演算法 \_ WEBCREDENTIALS**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NCryptprotect。h</dt> </dl> |



 

 




