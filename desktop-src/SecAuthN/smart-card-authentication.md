---
description: 智慧卡驗證
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: 智慧卡驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985032"
---
# <a name="smart-card-authentication"></a><span data-ttu-id="5339c-103">智慧卡驗證</span><span class="sxs-lookup"><span data-stu-id="5339c-103">Smart Card Authentication</span></span>

<span data-ttu-id="5339c-104">[*智慧卡子系統*](../secgloss/s-gly.md)的基本部分是根據 PC/SC 標準 (請參閱) 的規格 [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) 。</span><span class="sxs-lookup"><span data-stu-id="5339c-104">The basic parts of the [*smart card subsystem*](../secgloss/s-gly.md) are based on PC/SC standards (see the specifications at [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/)).</span></span> <span data-ttu-id="5339c-105">這些基本元件包括：</span><span class="sxs-lookup"><span data-stu-id="5339c-105">These basic parts include:</span></span>

-   <span data-ttu-id="5339c-106">使用 Windows API 的 [*資源管理員*](../secgloss/r-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="5339c-106">A [*resource manager*](../secgloss/r-gly.md) that uses a Windows API.</span></span>
-   <span data-ttu-id="5339c-107">可搭配資源管理員使用的 [*使用者介面*](../secgloss/u-gly.md) (UI) 。</span><span class="sxs-lookup"><span data-stu-id="5339c-107">A [*user interface*](../secgloss/u-gly.md) (UI) that works with the resource manager.</span></span>
-   <span data-ttu-id="5339c-108">提供特定服務存取權的數個基底 [*服務提供者*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="5339c-108">Several base [*service providers*](../secgloss/s-gly.md) that provide access to specific services.</span></span> <span data-ttu-id="5339c-109">相對於 resource manager 的 Windows API，服務提供者會使用 COM 介面模型來提供 [*智慧卡*](../secgloss/s-gly.md) 服務。</span><span class="sxs-lookup"><span data-stu-id="5339c-109">In contrast to the resource manager's Windows API, service providers use a COM interface model to provide [*smart card*](../secgloss/s-gly.md) services.</span></span>

<span data-ttu-id="5339c-110">下圖顯示這些元件在整體智慧卡架構中的關聯性。</span><span class="sxs-lookup"><span data-stu-id="5339c-110">The following illustration shows the relationships of these parts in the overall smart card architecture.</span></span>

![智慧卡架構](images/smartovr2a.png)

<span data-ttu-id="5339c-112">如需 [*智慧卡子系統*](../secgloss/s-gly.md) 如何與 Microsoft Internet Security Framework 中提供的其他服務搭配運作的詳細資訊，請參閱與 [其他服務相關](relation-to-other-services.md)的資訊。</span><span class="sxs-lookup"><span data-stu-id="5339c-112">For information about how the [*smart card subsystem*](../secgloss/s-gly.md) works with other services available in the Microsoft Internet Security Framework, see [Relation to Other Services](relation-to-other-services.md).</span></span>

<span data-ttu-id="5339c-113">如需智慧卡驗證的相關資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="5339c-113">For information about smart card authentication, see the following topics.</span></span>



| <span data-ttu-id="5339c-114">主題</span><span class="sxs-lookup"><span data-stu-id="5339c-114">Topics</span></span>                                                                      | <span data-ttu-id="5339c-115">目錄</span><span class="sxs-lookup"><span data-stu-id="5339c-115">Contents</span></span>                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5339c-116">智慧卡概念</span><span class="sxs-lookup"><span data-stu-id="5339c-116">Smart Card Concepts</span></span>](smart-card-concepts.md)<br/>                   | <span data-ttu-id="5339c-117">使用者與智慧卡之間互動的基本概念和描述。</span><span class="sxs-lookup"><span data-stu-id="5339c-117">Basic concepts and description of the interaction between users and smart cards.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="5339c-118">智慧卡 Resource Manager</span><span class="sxs-lookup"><span data-stu-id="5339c-118">Smart Card Resource Manager</span></span>](smart-card-resource-manager.md)<br/>   | <span data-ttu-id="5339c-119">資源管理員 API 的相關資訊，可管理 [*讀取器*](../secgloss/r-gly.md) 和 [*智慧卡*](../secgloss/s-gly.md)的存取權。</span><span class="sxs-lookup"><span data-stu-id="5339c-119">Information about the resource manager API, which manages the access to [*readers*](../secgloss/r-gly.md) and to [*smart cards*](../secgloss/s-gly.md).</span></span><br/> |
| [<span data-ttu-id="5339c-120">智慧卡消費者介面</span><span class="sxs-lookup"><span data-stu-id="5339c-120">Smart Card User Interface</span></span>](smart-card-user-interface.md)<br/>       | <span data-ttu-id="5339c-121">[ [*智慧卡一般] 對話方塊*](../secgloss/s-gly.md)的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5339c-121">Information about the [*smart card common dialog box*](../secgloss/s-gly.md).</span></span><br/>                                                                                   |
| [<span data-ttu-id="5339c-122">智慧卡服務提供者</span><span class="sxs-lookup"><span data-stu-id="5339c-122">Smart Card Service Providers</span></span>](smart-card-service-providers.md)<br/> | <span data-ttu-id="5339c-123">提供智慧卡功能之介面、命令和包裝函式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5339c-123">Information about interfaces, commands, and wrappers that provide smart card capabilities.</span></span><br/>                                                                                                                                              |



 

<span data-ttu-id="5339c-124">此外，您可以在中找到目前的 Microsoft 智慧卡開發 [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) 。</span><span class="sxs-lookup"><span data-stu-id="5339c-124">Additionally, current Microsoft smart card developments can be found at [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx).</span></span>

 

 
