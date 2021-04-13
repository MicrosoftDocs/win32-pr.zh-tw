---
title: IKE/AuthIP 函數
description: " (WFP) 用來與金鑰郵件、網際網路金鑰交換 (IKE) 、網際網路金鑰交換 v2 (IKEv2) ，以及驗證的網際網路通訊協定 (AuthIP) 的函式。"
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- Windows 篩選平台 API 網際網路金鑰交換函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301392"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="33422-104">IKE/AuthIP 函數</span><span class="sxs-lookup"><span data-stu-id="33422-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="33422-105">Windows 篩選平台 (WFP) 用來與加密模組互動的函式（網際網路金鑰交換 (IKE) 、網際網路金鑰交換 v2 (IKEv2) ，以及驗證的網際網路通訊協定 (AuthIP) ）如下所示。</span><span class="sxs-lookup"><span data-stu-id="33422-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="33422-106">IkeextGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="33422-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="33422-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="33422-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="33422-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="33422-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="33422-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="33422-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="33422-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="33422-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="33422-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="33422-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="33422-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="33422-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="33422-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="33422-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="33422-114">IkeextSaEnum:</span><span class="sxs-lookup"><span data-stu-id="33422-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="33422-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="33422-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="33422-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="33422-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="33422-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8) </span><span class="sxs-lookup"><span data-stu-id="33422-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="33422-118">IkeextSaGetById:</span><span class="sxs-lookup"><span data-stu-id="33422-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="33422-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="33422-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="33422-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="33422-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="33422-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8) </span><span class="sxs-lookup"><span data-stu-id="33422-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 




