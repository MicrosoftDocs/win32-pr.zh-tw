---
description: 包含以字母 L 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: 'L (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33ee054c2bcf414ef289cc381ac13ef970da6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850516"
---
# <a name="l-security-glossary"></a>L (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [](u-gly.md) [](v-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) L [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**Ldap**
</dt> <dd>

查看 *輕量型目錄存取協定*

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**輕量型目錄存取協定**
</dt> <dd>

更容易實作為目錄服務之 X. 500 組標準的子集。

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**位元組由小到小**
</dt> <dd>

記憶體或資料格式，其中最不重要的位元組會儲存在較低的位址或第一次到達。

另請參閱 [*位元組由大到*](b-gly.md)小。

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**本機唯一識別碼**
</dt> <dd>

 (LUID) 64 位的值，此值保證在系統重新開機之前產生它的作業系統上是唯一的。

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**本機註冊授權單位**
</dt> <dd>

 (LRA) 發行者與 [*憑證授權單位*](c-gly.md) 單位之間的媒介 (CA) 。 例如，LRA 可以先驗證發行者的認證，再將其傳送至 CA。

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**本地安全機構**
</dt> <dd>

 (LSA) 受保護的子系統，可驗證使用者並將其記錄到本機系統。 LSA 也會維護系統上本機安全性的所有層面的相關資訊，統稱為系統的本機安全性原則。

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**邏輯存放區**
</dt> <dd>

請參閱 [*虛擬存放區*](v-gly.md)。

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**登入資料**
</dt> <dd>

[*安全性主體*](s-gly.md)為了進行驗證而呈現給系統的資訊。

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**登入識別碼**
</dt> <dd>

識別 *登入會話* 的 LUID。 登入識別碼在使用者登出之前有效。 當電腦正在執行時，登入識別碼是唯一的;沒有其他登入會話將會有相同的登入識別碼。 但是，當電腦啟動時，可能會重設登入識別碼的集合。 若要從 [*存取權杖*](a-gly.md)取出登入識別碼，請呼叫 TokenStatistics 的 **GetTokenInformation** 函數;登入識別碼位於 **AuthenticationId** 成員中。

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**登入會話**
</dt> <dd>

每次使用者登入電腦時，就會開始登入會話。 登入會話中的所有進程都有相同的主要 [*存取權杖*](a-gly.md)。 存取權杖包含登入會話安全性內容的相關資訊，包括使用者的 SID、 *登入識別碼*，以及 *登入 SID*。

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**登入 SID**
</dt> <dd>

識別 *登入會話* (SID) 的 [*安全識別碼*](s-gly.md)。 您可以使用 [*DACL*](d-gly.md) 中的登入 SID 來控制登入會話期間的存取權。 登入 SID 在使用者登出之前有效。 當電腦正在執行時，登入 SID 是唯一的;沒有其他登入會話將會有相同的登入 SID。 但是，當電腦啟動時，可能會重設登入 Sid 的組合。 若要從 [*存取權杖*](a-gly.md)取出登入 SID，請呼叫 TokenGroups 的 **GetTokenInformation** 函式。

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**低層級訊息函數**
</dt> <dd>

在比基底密碼編譯功能更高層級運作的訊息管理功能。 這些函式提供編碼資料的功能，以及解碼已接收的資料。 低層級的訊息函式比簡化的訊息函式提供更大的彈性，但需要更多函式呼叫。

另請參閱 [*簡化的訊息函數*](s-gly.md)。

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**Lsa**
</dt> <dd>

請參閱 *本地安全機構*。

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

請參閱 *本機唯一的識別碼*。

</dd> </dl>

 

 



