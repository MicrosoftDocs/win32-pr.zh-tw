---
description: Microsoft 在 Windows 2000 中引進了 (DPAPI) 的資料保護應用程式設計介面。
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973008"
---
# <a name="cng-dpapi"></a><span data-ttu-id="6e1f8-103">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="6e1f8-103">CNG DPAPI</span></span>

<span data-ttu-id="6e1f8-104">Microsoft 在 Windows 2000 中引進了 (DPAPI) 的資料保護應用程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="6e1f8-105">API 包含兩個函數： [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="6e1f8-106">DPAPI 是 CryptoAPI 的一部分，適用于只知道使用加密功能的開發人員。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="6e1f8-107">這兩個函數可用來加密和解密單一電腦上的靜態資料。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="6e1f8-108">不過，雲端運算通常需要在一部電腦上加密內容，才能在另一部電腦上解密。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="6e1f8-109">因此，從 Windows 8 開始，Microsoft 擴充了使用相當簡單的 API 來包含雲端案例的概念。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="6e1f8-110">這個新的 API （稱為 DPAPI）可讓您安全地共用秘密 (金鑰、密碼、金鑰材料) 和訊息，方法是保護這些秘密，以在適當的驗證和授權之後，用來在不同電腦上解除保護這些秘密。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="6e1f8-111">目前支援下列主體：</span><span class="sxs-lookup"><span data-stu-id="6e1f8-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="6e1f8-112">Active Directory 樹系中的群組。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="6e1f8-113">Web 認證。</span><span class="sxs-lookup"><span data-stu-id="6e1f8-113">Web credentials.</span></span>

<span data-ttu-id="6e1f8-114">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="6e1f8-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="6e1f8-115">保護提供者</span><span class="sxs-lookup"><span data-stu-id="6e1f8-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="6e1f8-116">保護描述項</span><span class="sxs-lookup"><span data-stu-id="6e1f8-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="6e1f8-117">受保護的資料格式</span><span class="sxs-lookup"><span data-stu-id="6e1f8-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="6e1f8-118">DPAPI-NG 建置於新一代密碼編譯 (CNG) 之上，並包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="6e1f8-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="6e1f8-119">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="6e1f8-120">**NCryptCloseProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="6e1f8-121">**NCryptProtectSecret**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="6e1f8-122">**NCryptQueryProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="6e1f8-123">**NCryptRegisterProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="6e1f8-124">**NCryptStreamClose**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="6e1f8-125">**NCryptStreamOpenToProtect**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="6e1f8-126">**NCryptStreamOpenToUnprotect**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="6e1f8-127">**NCryptStreamUpdate**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="6e1f8-128">**NCryptUnprotectSecret**</span><span class="sxs-lookup"><span data-stu-id="6e1f8-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
