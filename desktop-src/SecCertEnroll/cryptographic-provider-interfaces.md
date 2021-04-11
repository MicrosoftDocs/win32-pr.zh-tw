---
description: 下列介面可以用來取得密碼編譯提供者的相關資訊。
ms.assetid: f4f6a763-707d-48a2-acb9-2a0c3530cf6b
title: 密碼編譯提供者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fa42a9a2704849552fadeb79933d85df9e9f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113772"
---
# <a name="cryptographic-provider-interfaces"></a><span data-ttu-id="ed4f7-103">密碼編譯提供者介面</span><span class="sxs-lookup"><span data-stu-id="ed4f7-103">Cryptographic Provider Interfaces</span></span>

<span data-ttu-id="ed4f7-104">下列介面可以用來取得密碼編譯提供者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-104">The following interfaces can be used to retrieve information about cryptographic providers.</span></span>



| <span data-ttu-id="ed4f7-105">介面</span><span class="sxs-lookup"><span data-stu-id="ed4f7-105">Interface</span></span>                                    | <span data-ttu-id="ed4f7-106">描述</span><span class="sxs-lookup"><span data-stu-id="ed4f7-106">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="ed4f7-107">**ICspAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="ed4f7-107">**ICspAlgorithm**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)       | <span data-ttu-id="ed4f7-108">代表密碼編譯提供者所執行的演算法。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-108">Represents an algorithm implemented by a cryptographic provider.</span></span>             |
| [<span data-ttu-id="ed4f7-109">**ICspAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="ed4f7-109">**ICspAlgorithms**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)     | <span data-ttu-id="ed4f7-110">管理 [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-110">Manages a collection of [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span> |
| [<span data-ttu-id="ed4f7-111">**ICspInformation**</span><span class="sxs-lookup"><span data-stu-id="ed4f7-111">**ICspInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)   | <span data-ttu-id="ed4f7-112">提供有關密碼編譯提供者之一般資訊的存取權。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-112">Provides access to general information about a cryptographic provider.</span></span>       |
| [<span data-ttu-id="ed4f7-113">**ICspInformations**</span><span class="sxs-lookup"><span data-stu-id="ed4f7-113">**ICspInformations**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) | <span data-ttu-id="ed4f7-114">管理 [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-114">Manages a collection of [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) objects.</span></span>  |
| [<span data-ttu-id="ed4f7-115">**ICspStatus**</span><span class="sxs-lookup"><span data-stu-id="ed4f7-115">**ICspStatus**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus)             | <span data-ttu-id="ed4f7-116">包含密碼編譯提供者/演算法配對的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-116">Contains information about a cryptographic provider/algorithm pair.</span></span>          |
| [<span data-ttu-id="ed4f7-117">**ICspStatuses**</span><span class="sxs-lookup"><span data-stu-id="ed4f7-117">**ICspStatuses**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatuses)         | <span data-ttu-id="ed4f7-118">管理 [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="ed4f7-118">Manages a collection of [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) objects.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="ed4f7-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed4f7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed4f7-120">CertEnroll 介面</span><span class="sxs-lookup"><span data-stu-id="ed4f7-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



