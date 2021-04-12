---
title: TPM 基本服務
description: TPM 軟體提供服務作為透過遠端程序呼叫所公開的 API。 使用 TPM 來建立 TPM 模組。
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- TPM 基礎服務 TB
- TPM 基礎服務 TB 版，首頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376045"
---
# <a name="tpm-base-services"></a><span data-ttu-id="f78eb-106">TPM 基本服務</span><span class="sxs-lookup"><span data-stu-id="f78eb-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="f78eb-107">目的</span><span class="sxs-lookup"><span data-stu-id="f78eb-107">Purpose</span></span>

<span data-ttu-id="f78eb-108">信賴平臺模組 (TPM) 基礎服務 (TB) 功能會跨應用程式集中進行 TPM 存取。</span><span class="sxs-lookup"><span data-stu-id="f78eb-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="f78eb-109">[TB] 功能在 Windows Server 2008、Windows Vista 或更新版本的作業系統中會以系統服務的形式執行。</span><span class="sxs-lookup"><span data-stu-id="f78eb-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="f78eb-110">它會將服務提供給透過遠端程序呼叫（ (RPC) ）公開的 API。</span><span class="sxs-lookup"><span data-stu-id="f78eb-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="f78eb-111">[TB] 功能使用由呼叫應用程式以合作排程 TPM 存取所指定的優先順序。</span><span class="sxs-lookup"><span data-stu-id="f78eb-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="f78eb-112">TPM 可用於金鑰儲存體作業。</span><span class="sxs-lookup"><span data-stu-id="f78eb-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="f78eb-113">不過，我們鼓勵開發人員改用這些案例的 [金鑰儲存體 api](/windows/desktop/SecCNG/key-storage-and-retrieval) 。</span><span class="sxs-lookup"><span data-stu-id="f78eb-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="f78eb-114">金鑰儲存體 Api 提供的功能，可讓您建立、簽署或加密密碼編譯金鑰，並保存密碼編譯金鑰，而且比起這些目標案例的 TB 更高階且更容易使用。</span><span class="sxs-lookup"><span data-stu-id="f78eb-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="f78eb-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="f78eb-115">Developer audience</span></span>

<span data-ttu-id="f78eb-116">當應用程式開發人員以 Windows 作業系統為基礎時，可使用此 TB。</span><span class="sxs-lookup"><span data-stu-id="f78eb-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="f78eb-117">開發人員應該熟悉 C 和 c + + 程式設計語言和 Microsoft Windows 程式設計環境。</span><span class="sxs-lookup"><span data-stu-id="f78eb-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f78eb-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="f78eb-118">Run-time requirements</span></span>

<span data-ttu-id="f78eb-119">[TB] 功能至少需要 Windows Server 2008 或 Windows Vista 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f78eb-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="f78eb-120">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="f78eb-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f78eb-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="f78eb-121">In this section</span></span>



| <span data-ttu-id="f78eb-122">主題</span><span class="sxs-lookup"><span data-stu-id="f78eb-122">Topic</span></span>                                         | <span data-ttu-id="f78eb-123">描述</span><span class="sxs-lookup"><span data-stu-id="f78eb-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f78eb-124">關於 TB</span><span class="sxs-lookup"><span data-stu-id="f78eb-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="f78eb-125">最重要的概念，以及更高階的 TBS 功能觀點。</span><span class="sxs-lookup"><span data-stu-id="f78eb-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="f78eb-126">使用 TB</span><span class="sxs-lookup"><span data-stu-id="f78eb-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="f78eb-127">使用 TB API 的最 TB 程式和程式。</span><span class="sxs-lookup"><span data-stu-id="f78eb-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="f78eb-128">TB 參考</span><span class="sxs-lookup"><span data-stu-id="f78eb-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="f78eb-129">有關 TB 函數、結構和傳回碼的檔。</span><span class="sxs-lookup"><span data-stu-id="f78eb-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

