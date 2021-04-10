---
description: Xenroll.dll 程式庫已從作業系統中移除，並由 CertEnroll.dll 取代。
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: 將 Xenroll.dll 對應至 CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694015"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="d50cc-103">將 Xenroll.dll 對應至 CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="d50cc-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="d50cc-104">在 Windows Vista 之前，憑證註冊控制項已在 Xenroll.dll 中執行。</span><span class="sxs-lookup"><span data-stu-id="d50cc-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="d50cc-105">Xenroll.dll 程式庫已從作業系統中移除，並由 CertEnroll.dll 取代。</span><span class="sxs-lookup"><span data-stu-id="d50cc-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="d50cc-106">Xenroll.dll 嘗試執行兩個平行的介面集。</span><span class="sxs-lookup"><span data-stu-id="d50cc-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="d50cc-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll)、 [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2)、 [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)和 [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) 符合自動化規範，且與指令碼語言相容。</span><span class="sxs-lookup"><span data-stu-id="d50cc-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="d50cc-108">對應的介面（[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll)、 [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)和 [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)）無法編寫腳本，但更方便 c + + 程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="d50cc-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="d50cc-109">當它們演進時，兩組介面不會保持同步。</span><span class="sxs-lookup"><span data-stu-id="d50cc-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="d50cc-110">尤其是， **ICEnroll4** 最近表示的雙重介面集會定義 **IEnroll4** 所定義的功能子集。</span><span class="sxs-lookup"><span data-stu-id="d50cc-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="d50cc-111">CertEnroll.dll 會採用一組較大型且更具結構化的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="d50cc-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="d50cc-112">下列主題討論 Xenroll.dll 如何對應至不同類型功能的 CertEnroll.dll。</span><span class="sxs-lookup"><span data-stu-id="d50cc-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="d50cc-113">憑證要求功能</span><span class="sxs-lookup"><span data-stu-id="d50cc-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="d50cc-114">憑證回應功能</span><span class="sxs-lookup"><span data-stu-id="d50cc-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="d50cc-115">屬性函式</span><span class="sxs-lookup"><span data-stu-id="d50cc-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="d50cc-116">擴充功能</span><span class="sxs-lookup"><span data-stu-id="d50cc-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="d50cc-117">外部屬性函式</span><span class="sxs-lookup"><span data-stu-id="d50cc-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="d50cc-118">私用和公開金鑰函數</span><span class="sxs-lookup"><span data-stu-id="d50cc-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="d50cc-119">密碼編譯服務提供者函數</span><span class="sxs-lookup"><span data-stu-id="d50cc-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="d50cc-120">憑證存放區功能</span><span class="sxs-lookup"><span data-stu-id="d50cc-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="d50cc-121">個人資訊交換功能</span><span class="sxs-lookup"><span data-stu-id="d50cc-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="d50cc-122">Helper 函式</span><span class="sxs-lookup"><span data-stu-id="d50cc-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="d50cc-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="d50cc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d50cc-124">使用憑證註冊 API</span><span class="sxs-lookup"><span data-stu-id="d50cc-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
