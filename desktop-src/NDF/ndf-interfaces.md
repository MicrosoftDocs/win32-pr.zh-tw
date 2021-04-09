---
title: NDF 介面
description: 下列介面可以用來擴充識別為可延伸的 Microsoft Helper 類別的功能。
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020721"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="0b93f-103">NDF 介面</span><span class="sxs-lookup"><span data-stu-id="0b93f-103">NDF Interfaces</span></span>

<span data-ttu-id="0b93f-104">下列介面可以用來擴充識別為可延伸的 Microsoft Helper 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="0b93f-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="0b93f-105">雖然大部分的應用程式都不需要這項功能，但在某些情況下，它可以提供更具體的診斷和解決方式。</span><span class="sxs-lookup"><span data-stu-id="0b93f-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="0b93f-106">這些介面及其相關聯的方法適用于執行自己的協力廠商協助程式類別的程式開發人員，以擴充 NDF 功能。</span><span class="sxs-lookup"><span data-stu-id="0b93f-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="0b93f-107">介面名稱</span><span class="sxs-lookup"><span data-stu-id="0b93f-107">Interface Name</span></span>                                                 | <span data-ttu-id="0b93f-108">描述</span><span class="sxs-lookup"><span data-stu-id="0b93f-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b93f-109">**INetDiagHelper**</span><span class="sxs-lookup"><span data-stu-id="0b93f-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="0b93f-110">由 NDF 針對診斷期間發生的大部分活動呼叫。</span><span class="sxs-lookup"><span data-stu-id="0b93f-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="0b93f-111">**INetDiagHelperEx**</span><span class="sxs-lookup"><span data-stu-id="0b93f-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="0b93f-112">由 NDF 呼叫來捕捉和提供與網路相關問題之診斷和解決的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b93f-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="0b93f-113">**INetDiagHelperInfo**</span><span class="sxs-lookup"><span data-stu-id="0b93f-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="0b93f-114">由 NDF 呼叫以驗證它有必要的資訊</span><span class="sxs-lookup"><span data-stu-id="0b93f-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="0b93f-115">**INetDiagHelperUtilFactory**</span><span class="sxs-lookup"><span data-stu-id="0b93f-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="0b93f-116">保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="0b93f-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 




