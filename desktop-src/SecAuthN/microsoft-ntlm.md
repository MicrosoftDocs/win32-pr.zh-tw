---
description: Windows 挑戰/回應 (NTLM) 是在網路上使用的驗證通訊協定，該通訊協定包含執行 Windows 作業系統和獨立系統的系統。
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511236"
---
# <a name="microsoft-ntlm"></a><span data-ttu-id="e712f-103">Microsoft NTLM</span><span class="sxs-lookup"><span data-stu-id="e712f-103">Microsoft NTLM</span></span>

<span data-ttu-id="e712f-104">Windows 挑戰/回應 (NTLM) 是在網路上使用的驗證通訊協定，該通訊協定包含執行 Windows 作業系統和獨立系統的系統。</span><span class="sxs-lookup"><span data-stu-id="e712f-104">Windows Challenge/Response (NTLM) is the authentication protocol used on networks that include systems running the Windows operating system and on stand-alone systems.</span></span>

<span data-ttu-id="e712f-105">Microsoft [*Kerberos*](../secgloss/k-gly.md) [*安全性套件*](../secgloss/s-gly.md) 可為網路上的系統增加更高的安全性。</span><span class="sxs-lookup"><span data-stu-id="e712f-105">The Microsoft [*Kerberos*](../secgloss/k-gly.md) [*security package*](../secgloss/s-gly.md) adds greater security than NTLM to systems on a network.</span></span> <span data-ttu-id="e712f-106">雖然 Microsoft *Kerberos* 是所選擇的通訊協定，但仍支援 NTLM。</span><span class="sxs-lookup"><span data-stu-id="e712f-106">Although Microsoft *Kerberos* is the protocol of choice, NTLM is still supported.</span></span> <span data-ttu-id="e712f-107">NTLM 還必須用於獨立系統的登入驗證。</span><span class="sxs-lookup"><span data-stu-id="e712f-107">NTLM must also be used for logon authentication on stand-alone systems.</span></span> <span data-ttu-id="e712f-108">如需有關 Kerberos 的詳細資訊，請參閱 [Microsoft kerberos](microsoft-kerberos.md)。</span><span class="sxs-lookup"><span data-stu-id="e712f-108">For more information about Kerberos, see [Microsoft Kerberos](microsoft-kerberos.md).</span></span>

<span data-ttu-id="e712f-109">NTLM 認證是以互動式登入程式期間取得的資料為基礎，並且包含功能變數名稱、使用者名稱和使用者密碼的單向 [*雜湊*](../secgloss/h-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="e712f-109">NTLM credentials are based on data obtained during the interactive logon process and consist of a domain name, a user name, and a one-way [*hash*](../secgloss/h-gly.md) of the user's password.</span></span> <span data-ttu-id="e712f-110">NTLM 使用加密的挑戰/回應通訊協定來驗證使用者，而不需要透過網路傳送使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="e712f-110">NTLM uses an encrypted challenge/response protocol to authenticate a user without sending the user's password over the wire.</span></span> <span data-ttu-id="e712f-111">相反地，要求驗證的系統必須執行計算，以證明它可以存取安全的 NTLM 認證。</span><span class="sxs-lookup"><span data-stu-id="e712f-111">Instead, the system requesting authentication must perform a calculation that proves it has access to the secured NTLM credentials.</span></span>

<span data-ttu-id="e712f-112">透過網路的互動式 NTLM 驗證通常牽涉到兩個系統：用戶端系統（使用者要求驗證的用戶端系統），以及網域控制站，其中會保留與使用者密碼相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="e712f-112">Interactive NTLM authentication over a network typically involves two systems: a client system, where the user is requesting authentication, and a domain controller, where information related to the user's password is kept.</span></span> <span data-ttu-id="e712f-113">非互動式驗證（可能需要允許已登入的使用者存取資源，例如伺服器應用程式），通常需要三個系統：用戶端、伺服器，以及代表伺服器進行驗證計算的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="e712f-113">Noninteractive authentication, which may be required to permit an already logged-on user to access a resource such as a server application, typically involves three systems: a client, a server, and a domain controller that does the authentication calculations on behalf of the server.</span></span>

<span data-ttu-id="e712f-114">下列步驟顯示 NTLM 非互動式驗證的大綱。</span><span class="sxs-lookup"><span data-stu-id="e712f-114">The following steps present an outline of NTLM noninteractive authentication.</span></span> <span data-ttu-id="e712f-115">第一個步驟會提供使用者的 NTLM 認證，而且只會在互動式驗證 (登入) 處理過程中發生。</span><span class="sxs-lookup"><span data-stu-id="e712f-115">The first step provides the user's NTLM credentials and occurs only as part of the interactive authentication (logon) process.</span></span>

1.  <span data-ttu-id="e712f-116">只有在使用者存取用戶端電腦並提供功能變數名稱、使用者名稱和密碼時，) 才 (互動式驗證。</span><span class="sxs-lookup"><span data-stu-id="e712f-116">(Interactive authentication only) A user accesses a client computer and provides a domain name, user name, and password.</span></span> <span data-ttu-id="e712f-117">用戶端會計算密碼的密碼編譯 [*雜湊*](../secgloss/h-gly.md) ，並捨棄實際的密碼。</span><span class="sxs-lookup"><span data-stu-id="e712f-117">The client computes a cryptographic [*hash*](../secgloss/h-gly.md) of the password and discards the actual password.</span></span>
2.  <span data-ttu-id="e712f-118">用戶端會將使用者名稱以 [*純文字*](../secgloss/p-gly.md)) 傳送至伺服器 (。</span><span class="sxs-lookup"><span data-stu-id="e712f-118">The client sends the user name to the server (in [*plaintext*](../secgloss/p-gly.md)).</span></span>
3.  <span data-ttu-id="e712f-119">伺服器會產生16位元組的亂數字（稱為 *挑戰* 或 [*nonce*](../secgloss/n-gly.md)），並將它傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="e712f-119">The server generates a 16-byte random number, called a *challenge* or [*nonce*](../secgloss/n-gly.md), and sends it to the client.</span></span>
4.  <span data-ttu-id="e712f-120">用戶端會使用使用者密碼的雜湊來加密這項挑戰，並將結果傳回伺服器。</span><span class="sxs-lookup"><span data-stu-id="e712f-120">The client encrypts this challenge with the hash of the user's password and returns the result to the server.</span></span> <span data-ttu-id="e712f-121">這稱為 *回應*。</span><span class="sxs-lookup"><span data-stu-id="e712f-121">This is called the *response*.</span></span>
5.  <span data-ttu-id="e712f-122">伺服器會將下列三個專案傳送至網域控制站：</span><span class="sxs-lookup"><span data-stu-id="e712f-122">The server sends the following three items to the domain controller:</span></span>

    -   <span data-ttu-id="e712f-123">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="e712f-123">User name</span></span>
    -   <span data-ttu-id="e712f-124">傳送至用戶端的挑戰</span><span class="sxs-lookup"><span data-stu-id="e712f-124">Challenge sent to the client</span></span>
    -   <span data-ttu-id="e712f-125">從用戶端收到的回應</span><span class="sxs-lookup"><span data-stu-id="e712f-125">Response received from the client</span></span>

6.  <span data-ttu-id="e712f-126">網域控制站會使用使用者名稱，從安全性帳戶管理員資料庫取出使用者密碼的雜湊。</span><span class="sxs-lookup"><span data-stu-id="e712f-126">The domain controller uses the user name to retrieve the hash of the user's password from the Security Account Manager database.</span></span> <span data-ttu-id="e712f-127">它會使用此密碼雜湊來加密挑戰。</span><span class="sxs-lookup"><span data-stu-id="e712f-127">It uses this password hash to encrypt the challenge.</span></span>
7.  <span data-ttu-id="e712f-128">網域控制站會比較在步驟6中所計算 (的加密挑戰，) 到步驟 4) 中用戶端 (所計算的回應。</span><span class="sxs-lookup"><span data-stu-id="e712f-128">The domain controller compares the encrypted challenge it computed (in step 6) to the response computed by the client (in step 4).</span></span> <span data-ttu-id="e712f-129">如果兩者相同，驗證就會成功。</span><span class="sxs-lookup"><span data-stu-id="e712f-129">If they are identical, authentication is successful.</span></span>

<span data-ttu-id="e712f-130">您的應用程式不應直接存取 NTLM [*安全性封裝*](../secgloss/s-gly.md) ;相反地，它應該使用 [*Negotiate*](../secgloss/n-gly.md) 安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="e712f-130">Your application should not access the NTLM [*security package*](../secgloss/s-gly.md) directly; instead, it should use the [*Negotiate*](../secgloss/n-gly.md) security package.</span></span> <span data-ttu-id="e712f-131">Negotiate 可讓您的應用程式利用更高階的 [*安全性通訊協定*](../secgloss/s-gly.md) （如果驗證所含的系統支援的話）。</span><span class="sxs-lookup"><span data-stu-id="e712f-131">Negotiate allows your application to take advantage of more advanced [*security protocols*](../secgloss/s-gly.md) if they are supported by the systems involved in the authentication.</span></span> <span data-ttu-id="e712f-132">目前，協商安全性封裝會在 [*Kerberos*](../secgloss/k-gly.md) 和 NTLM 之間進行選取。</span><span class="sxs-lookup"><span data-stu-id="e712f-132">Currently, the Negotiate security package selects between [*Kerberos*](../secgloss/k-gly.md) and NTLM.</span></span> <span data-ttu-id="e712f-133">除非其中一個與驗證相關的系統無法使用，否則 Negotiate 會選取 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="e712f-133">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication.</span></span>

 

 
