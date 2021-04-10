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
# <a name="i-security-glossary"></a><span data-ttu-id="bbd6b-103">我 (安全性詞彙) </span><span class="sxs-lookup"><span data-stu-id="bbd6b-103">I (Security Glossary)</span></span>

<span data-ttu-id="bbd6b-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [](u-gly.md) [](v-gly.md) [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="bbd6b-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bbd6b-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**Iis**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-106">支援網站建立、設定和管理，以及其他網際網路功能的軟體服務。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-106">Software services that support website creation, configuration, and management, along with other Internet functions.</span></span> <span data-ttu-id="bbd6b-107">Internet Information Services 包括網路新聞傳輸通訊協定 (NNTP) 、檔案傳輸通訊協定 (FTP) ，以及簡易郵件傳送通訊協定 (SMTP) 。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-107">Internet Information Services include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP), and Simple Mail Transfer Protocol (SMTP).</span></span> <span data-ttu-id="bbd6b-108">IIS 納入了各種安全性功能、允許 CGI 應用程式，並提供 Gopher 和 FTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-108">IIS incorporates various functions for security, allows for CGI applications, and provides for Gopher and FTP servers.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**類比**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-110">一種機制，可讓伺服器進程使用用戶端的安全性認證或使用認證的其他使用者來執行。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-110">A mechanism that allows a server process to run by using the security credentials of the client or some other user using the credentials.</span></span> <span data-ttu-id="bbd6b-111">當伺服器模擬用戶端時，伺服器執行的任何作業都會使用用戶端的 (模擬使用者的) 認證來執行。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-111">When the server is impersonating the client, any operations performed by the server are performed by using the client's (impersonating user's) credentials.</span></span> <span data-ttu-id="bbd6b-112">模擬不允許伺服器代表用戶端存取遠端資源。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-112">Impersonation does not allow the server to access remote resources on behalf of the client.</span></span> <span data-ttu-id="bbd6b-113">這需要委派。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-113">This requires delegation.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**模擬權杖**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**impersonation token**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-115">已建立來捕捉用戶端進程安全性資訊的存取權杖，可讓伺服器「模擬」安全性作業中的用戶端進程。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-115">An access token that has been created to capture the security information of a client process, allowing a server to "impersonate" the client process in security operations.</span></span>

<span data-ttu-id="bbd6b-116">另請參閱 [*存取權杖*](a-gly.md) 和 [*主要權杖*](p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-116">See also [*access token*](a-gly.md) and [*primary token*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**初始化向量**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**initialization vector**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-118"> (IV) 在以區塊加密加密之前附加到純文字前面的隨機位元組序列。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-118">(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher.</span></span> <span data-ttu-id="bbd6b-119">將初始化向量新增至純文字的開頭，可避免任何兩個訊息的初始加密文字區塊都相同。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-119">Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages.</span></span> <span data-ttu-id="bbd6b-120">例如，如果訊息一律以一般標頭開頭 (信頭或 "From" 行) 它們的初始加密文字一律相同，前提是使用相同的密碼編譯演算法和對稱金鑰。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-120">For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used.</span></span> <span data-ttu-id="bbd6b-121">新增隨機初始化向量可避免發生此情況。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-121">Adding a random initialization vector eliminates this from happening.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**內部資料**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**inner data**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-123">當做另一個已編碼訊息的訊息使用的任何編碼資料。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-123">Any encoded data used as the message for another encoded message.</span></span> <span data-ttu-id="bbd6b-124">例如，封包訊息及其雜湊值可能是第二個訊息的內部資料。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-124">For example, an enveloped message and its hash value may be the inner data for a second message.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**內部內容**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**inner content**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-126">增強的資料，例如使用數位簽章。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-126">Data that is enhanced, such as with a digital signature.</span></span> <span data-ttu-id="bbd6b-127">此詞彙主要用於討論 PKCS 7 訊息中的增強型資料 \# 。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-127">This term is used primarily when discussing enhanced data in a PKCS \#7 message.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**誠信**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrity**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-129">訊息傳送或儲存之後的完整性和精確度。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-129">The completeness and accuracy of a message after it has been sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**完整性 SID**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**integrity SID**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-131">代表完整性層級 (SID) 的 [*安全識別碼*](s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-131">A [*security identifier*](s-gly.md) (SID) that represents an integrity level.</span></span> <span data-ttu-id="bbd6b-132">[*系統存取控制清單*](s-gly.md)中的完整性 SID (物件安全描述項的 SACL) 會指定物件的完整性層級。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-132">An integrity SID in the [*system access control list*](s-gly.md) (SACL) of an object's security descriptor specifies the integrity level of the object.</span></span> <span data-ttu-id="bbd6b-133">存取權杖中的完整性 Sid 會指定權杖的完整性層級。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-133">Integrity SIDs in an access token specify the integrity level of the token.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-135">插斷要求層級 (IRQL) 定義處理器在任何指定時間運作的硬體優先順序。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-135">An interrupt request level (IRQL) defines the hardware priority at which a processor operates at any given time.</span></span> <span data-ttu-id="bbd6b-136">在 Windows Driver Model 中，以低個 IRQL 執行的執行緒可能會中斷，以較高的 IRQL 執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-136">In the Windows Driver Model, a thread running at a low IRQL can be interrupted to run code at a higher IRQL.</span></span>

</dd> <dt>

<span data-ttu-id="bbd6b-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**四**</span><span class="sxs-lookup"><span data-stu-id="bbd6b-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span></span>
</dt> <dd>

<span data-ttu-id="bbd6b-138">請參閱 *初始化向量*。</span><span class="sxs-lookup"><span data-stu-id="bbd6b-138">See *initialization vector*.</span></span>

</dd> </dl>

 

 



