---
description: 使用 CryptoAPI 函式來管理憑證存放區和這些存放區中的憑證、憑證撤銷清單，以及憑證信任清單。
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: 使用憑證存放區管理憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554043"
---
# <a name="managing-certificates-with-certificate-stores"></a><span data-ttu-id="0b3e8-103">使用憑證存放區管理憑證</span><span class="sxs-lookup"><span data-stu-id="0b3e8-103">Managing Certificates with Certificate Stores</span></span>

<span data-ttu-id="0b3e8-104">經過一段時間後， [*憑證*](../secgloss/c-gly.md) 就會累積在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-104">Over a period of time, [*certificates*](../secgloss/c-gly.md) will accumulate on a user's computer.</span></span> <span data-ttu-id="0b3e8-105">需要工具才能管理這些憑證。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-105">Tools are required to manage these certificates.</span></span> <span data-ttu-id="0b3e8-106">[*CryptoAPI*](../secgloss/c-gly.md) 提供這些工具作為函式來儲存、取出、刪除、列出 (列舉) ，以及驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-106">[*CryptoAPI*](../secgloss/c-gly.md) provides those tools as functions to store, retrieve, delete, list (enumerate), and verify certificates.</span></span> <span data-ttu-id="0b3e8-107">CryptoAPI 也提供將憑證附加至訊息的方法。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-107">CryptoAPI also provides the means to attach certificates to messages.</span></span>

<span data-ttu-id="0b3e8-108">CryptoAPI 提供兩種主要的函式類別來管理憑證：管理 [*憑證存放區*](../secgloss/c-gly.md)的函式、用來處理憑證的函式、 [*憑證撤銷清單*](../secgloss/c-gly.md) (crl) ，以及在這些存放區內 (ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-108">CryptoAPI offers two main categories of functions for managing certificates: functions that manage [*certificate stores*](../secgloss/c-gly.md), and functions that work with the certificates, [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) within those stores.</span></span>

<span data-ttu-id="0b3e8-109">管理 [*憑證存放區*](../secgloss/c-gly.md) 的函式包含使用邏輯或 [*虛擬存放區*](../secgloss/v-gly.md)、 [*遠端存放*](../secgloss/r-gly.md)區、 [*外部*](../secgloss/e-gly.md)存放區，以及可重新放置之存放區的功能。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-109">The functions that manage [*certificate stores*](../secgloss/c-gly.md) include functions for working with logical or [*virtual stores*](../secgloss/v-gly.md), [*remote stores*](../secgloss/r-gly.md), [*external stores*](../secgloss/e-gly.md), and stores that can be relocated.</span></span>

<span data-ttu-id="0b3e8-110">憑證、 [*crl*](../secgloss/c-gly.md)和 [*ctl*](../secgloss/c-gly.md) 可以保留並保留在 [*憑證存放區*](../secgloss/c-gly.md)中。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-110">Certificates, [*CRLs*](../secgloss/c-gly.md), and [*CTLs*](../secgloss/c-gly.md) can be kept and maintained in [*certificate stores*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="0b3e8-111">您可以從存放區的存放區中取出它們，以便在驗證程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-111">They can be retrieved from a store where they have been persisted for use in authentication processes.</span></span>

<span data-ttu-id="0b3e8-112">[*憑證存放區*](../secgloss/c-gly.md)是所有憑證功能的核心。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-112">The [*certificate store*](../secgloss/c-gly.md) is central to all certificate functionality.</span></span> <span data-ttu-id="0b3e8-113">憑證會在存放區中使用具有 "Cert" 前置詞的函式進行管理。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-113">The certificates are managed in the store using functions with a "Cert" prefix.</span></span> <span data-ttu-id="0b3e8-114">一般憑證存放區是連結的 [*憑證*](../secgloss/c-gly.md) 清單，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-114">A typical certificate store is a linked list of [*certificates*](../secgloss/c-gly.md) as shown in the following illustration.</span></span>

![憑證存放區](images/certstore1.png)

<span data-ttu-id="0b3e8-116">上圖顯示：</span><span class="sxs-lookup"><span data-stu-id="0b3e8-116">The preceding illustration shows:</span></span>

-   <span data-ttu-id="0b3e8-117">每個 [*憑證存放區*](../secgloss/c-gly.md) 都有指向該存放區中第一個憑證區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-117">Each [*certificate store*](../secgloss/c-gly.md) has a pointer to the first certificate block in that store.</span></span>
-   <span data-ttu-id="0b3e8-118">憑證區塊包含該憑證資料的指標，以及存放區中下一個憑證區塊的「下一步」指標。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-118">A certificate block includes a pointer to that certificate's data and a "next" pointer to the next certificate block in the store.</span></span>
-   <span data-ttu-id="0b3e8-119">最後一個憑證區塊中的「下一個」指標會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-119">The "next" pointer in the last certificate block is set to **NULL**.</span></span>
-   <span data-ttu-id="0b3e8-120">憑證的資料區塊包含唯讀憑證內容和憑證的任何擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-120">The data block of a certificate contains the read-only certificate context and any extended properties of the certificate.</span></span>
-   <span data-ttu-id="0b3e8-121">每個憑證的資料區塊都包含 [*參考計數*](../secgloss/r-gly.md) ，可追蹤存在之憑證的指標數目。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-121">The data block of each certificate contains a [*reference count*](../secgloss/r-gly.md) that keeps track of the number of pointers to the certificate that exist.</span></span>

<span data-ttu-id="0b3e8-122">[*憑證存放區*](../secgloss/c-gly.md)中的憑證通常會保留在某種永久儲存區中，例如磁片檔案或系統登錄。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-122">Certificates in a [*certificate store*](../secgloss/c-gly.md) are normally kept in some kind of permanent storage such as a disk file or the system registry.</span></span> <span data-ttu-id="0b3e8-123">憑證存放區也可以完全在記憶體中建立和開啟。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-123">Certificate stores can also be created and opened strictly in memory.</span></span> <span data-ttu-id="0b3e8-124">記憶體存放區提供暫時的憑證儲存體，可處理不需要保留的憑證。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-124">A memory store provides temporary certificate storage for working with certificates that do not need to be kept.</span></span>

<span data-ttu-id="0b3e8-125">其他存放區位置可讓存放區在本機電腦的登錄區中，或在遠端電腦的登錄中，以適當的許可權設定來保留及搜尋。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-125">Additional store locations allow stores to be kept and searched in various parts of a local computer's registry or, with proper permissions set, in the registry on a remote computer.</span></span>

<span data-ttu-id="0b3e8-126">每位使用者都有個人的存放區，其中儲存了該使用者的憑證。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-126">Each user has a personal My store where that user's certificates are stored.</span></span> <span data-ttu-id="0b3e8-127">「我的存放區」可以是許多實體位置的任意一個，包括本機或遠端電腦上的登錄、磁片檔案、資料庫、目錄服務、 [*智慧卡*](../secgloss/s-gly.md)或其他位置。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-127">The My store can be at any one of many physical locations, including the registry on a local or remote computer, a disk file, a database, directory service, a [*smart card*](../secgloss/s-gly.md), or another location.</span></span> <span data-ttu-id="0b3e8-128">雖然任何憑證都可以儲存在「我的存放區」中，但此存放區應保留給使用者的個人憑證：這些憑證用來簽署和解密該使用者的訊息。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-128">While any certificate can be stored in the My store, this store should be reserved for a user's personal certificates: those certificates used for signing and decrypting that user's messages.</span></span>

<span data-ttu-id="0b3e8-129">使用憑證進行驗證取決於擁有一些受信任的憑證簽發者所發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-129">Using certificates for authentication depends on having certificates issued by some trusted certificate issuer.</span></span> <span data-ttu-id="0b3e8-130">受信任的憑證簽發者的憑證通常會保留在根存放區中，且目前會保存到登錄子機碼中。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-130">Certificates for trusted certificate issuers are typically kept in the Root store, which is currently persisted to a registry subkey.</span></span> <span data-ttu-id="0b3e8-131">在 CryptoAPI 內容中，根存放區會受到保護，而使用者介面對話方塊會提醒使用者只將受信任的憑證放到該存放區中。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-131">In the CryptoAPI context, the Root store is protected, and user interface dialog boxes remind the user to place only trusted certificates into that store.</span></span> <span data-ttu-id="0b3e8-132">在商業網路的情況下，系統管理員可能會將憑證推送 (從網域控制站電腦) 複製到用戶端電腦上的根存放區。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-132">In enterprise network situations, certificates might be pushed (copied) by a system administrator from the domain controller computer to the Root stores on client computers.</span></span> <span data-ttu-id="0b3e8-133">此程式會提供具有類似信任清單之網域的所有成員。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-133">This process provides all members of a domain with similar trust lists.</span></span>

<span data-ttu-id="0b3e8-134">其他憑證可以存放在 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 系統存放區或使用者建立的檔案型存放區中。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-134">Other certificates can be stored in the [*certification authority*](../secgloss/c-gly.md) (CA) system store or in user-created, file-based stores.</span></span>

<span data-ttu-id="0b3e8-135">如需使用和維護憑證存放區的函式清單，請參閱 [憑證存放區功能](cryptography-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-135">For lists of functions for using and maintaining certificate stores, see [Certificate Store Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="0b3e8-136">如需使用其中一些函數的範例，請參閱 [範例 C 程式：憑證存放區作業](example-c-program-certificate-store-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="0b3e8-136">For an example that uses some of these functions, see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b3e8-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b3e8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b3e8-138">管理憑證存放區狀態</span><span class="sxs-lookup"><span data-stu-id="0b3e8-138">Managing a Certificate Store State</span></span>](managing-a-certificate-store-state.md)
</dt> <dt>

[<span data-ttu-id="0b3e8-139">使用憑證存放區中的憑證</span><span class="sxs-lookup"><span data-stu-id="0b3e8-139">Working with Certificates in Certificate Stores</span></span>](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[<span data-ttu-id="0b3e8-140">憑證連結</span><span class="sxs-lookup"><span data-stu-id="0b3e8-140">Certificate Links</span></span>](certificate-links.md)
</dt> <dt>

[<span data-ttu-id="0b3e8-141">集合存放區</span><span class="sxs-lookup"><span data-stu-id="0b3e8-141">Collection Stores</span></span>](collection-stores.md)
</dt> <dt>

[<span data-ttu-id="0b3e8-142">邏輯與實體存放區</span><span class="sxs-lookup"><span data-stu-id="0b3e8-142">Logical and Physical Stores</span></span>](logical-and-physical-stores.md)
</dt> <dt>

[<span data-ttu-id="0b3e8-143">系統存放區位置</span><span class="sxs-lookup"><span data-stu-id="0b3e8-143">System Store Locations</span></span>](system-store-locations.md)
</dt> <dt>

[<span data-ttu-id="0b3e8-144">憑證存放區遷移</span><span class="sxs-lookup"><span data-stu-id="0b3e8-144">Certificate Store Migration</span></span>](certificate-store-migration.md)
</dt> </dl>

 

 
