---
description: 包含以字母 I 開頭之安全性詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: '我 (安全性詞彙) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027088"
---
# <a name="i-security-glossary"></a>我 (安全性詞彙) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](u-gly.md) [](v-gly.md) [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**Iis**
</dt> <dd>

支援網站建立、設定和管理，以及其他網際網路功能的軟體服務。 Internet Information Services 包括網路新聞傳輸通訊協定 (NNTP) 、檔案傳輸通訊協定 (FTP) ，以及簡易郵件傳送通訊協定 (SMTP) 。 IIS 納入了各種安全性功能、允許 CGI 應用程式，並提供 Gopher 和 FTP 伺服器。

</dd> <dt>

<span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**類比**
</dt> <dd>

一種機制，可讓伺服器進程使用用戶端的安全性認證或使用認證的其他使用者來執行。 當伺服器模擬用戶端時，伺服器執行的任何作業都會使用用戶端的 (模擬使用者的) 認證來執行。 模擬不允許伺服器代表用戶端存取遠端資源。 這需要委派。

</dd> <dt>

<span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**模擬權杖**
</dt> <dd>

已建立來捕捉用戶端進程安全性資訊的存取權杖，可讓伺服器「模擬」安全性作業中的用戶端進程。

另請參閱 [*存取權杖*](a-gly.md) 和 [*主要權杖*](p-gly.md)。

</dd> <dt>

<span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**初始化向量**
</dt> <dd>

 (IV) 在以區塊加密加密之前附加到純文字前面的隨機位元組序列。 將初始化向量新增至純文字的開頭，可避免任何兩個訊息的初始加密文字區塊都相同。 例如，如果訊息一律以一般標頭開頭 (信頭或 "From" 行) 它們的初始加密文字一律相同，前提是使用相同的密碼編譯演算法和對稱金鑰。 新增隨機初始化向量可避免發生此情況。

</dd> <dt>

<span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**內部資料**
</dt> <dd>

當做另一個已編碼訊息的訊息使用的任何編碼資料。 例如，封包訊息及其雜湊值可能是第二個訊息的內部資料。

</dd> <dt>

<span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**內部內容**
</dt> <dd>

增強的資料，例如使用數位簽章。 此詞彙主要用於討論 PKCS 7 訊息中的增強型資料 \# 。

</dd> <dt>

<span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**誠信**
</dt> <dd>

訊息傳送或儲存之後的完整性和精確度。

</dd> <dt>

<span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**完整性 SID**
</dt> <dd>

代表完整性層級 (SID) 的 [*安全識別碼*](s-gly.md) 。 [*系統存取控制清單*](s-gly.md)中的完整性 SID (物件安全描述項的 SACL) 會指定物件的完整性層級。 存取權杖中的完整性 Sid 會指定權杖的完整性層級。

</dd> <dt>

<span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**
</dt> <dd>

插斷要求層級 (IRQL) 定義處理器在任何指定時間運作的硬體優先順序。 在 Windows Driver Model 中，以低個 IRQL 執行的執行緒可能會中斷，以較高的 IRQL 執行程式碼。

</dd> <dt>

<span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**四**
</dt> <dd>

請參閱 *初始化向量*。

</dd> </dl>

 

 



