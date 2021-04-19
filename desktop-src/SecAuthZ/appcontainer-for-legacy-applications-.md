---
description: AppContainer 環境是一個限制性的進程執行環境，可用於繼承應用程式以提供資源安全性。
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: 繼承應用程式的 AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b25ea292bdb8935375e50f669d17deb7efaef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990487"
---
# <a name="appcontainer-for-legacy-applications"></a><span data-ttu-id="cda86-103">繼承應用程式的 AppContainer</span><span class="sxs-lookup"><span data-stu-id="cda86-103">AppContainer for Legacy Applications</span></span>

<span data-ttu-id="cda86-104">AppContainer 環境是一個限制性的進程執行環境，可用於繼承應用程式以提供資源安全性。</span><span class="sxs-lookup"><span data-stu-id="cda86-104">The AppContainer environment is a restrictive process execution environment that can be used for legacy applications to provide resource security.</span></span> <span data-ttu-id="cda86-105">在 AppContainer 中執行的應用程式只能存取專門授與它的資源。</span><span class="sxs-lookup"><span data-stu-id="cda86-105">An application running in an AppContainer can only access resources specifically granted to it.</span></span> <span data-ttu-id="cda86-106">如此一來，在 AppContainer 中執行的應用程式將無法被駭客入侵，以允許在有限指派的資源以外的惡意動作。</span><span class="sxs-lookup"><span data-stu-id="cda86-106">As a result, applications implemented in an AppContainer cannot be hacked to allow malicious actions outside of the limited assigned resources.</span></span>

## <a name="benefits-of-using-an-appcontainer-environment"></a><span data-ttu-id="cda86-107">使用 AppContainer 環境的優點</span><span class="sxs-lookup"><span data-stu-id="cda86-107">Benefits of using an AppContainer environment</span></span>

<span data-ttu-id="cda86-108">AppContainer 環境提供應用程式的安全沙箱處理。</span><span class="sxs-lookup"><span data-stu-id="cda86-108">The AppContainer environment provides secure sandboxing of applications.</span></span> <span data-ttu-id="cda86-109">這會隔離應用程式，使其不需特定許可權即可存取硬體、檔案、登錄、其他應用程式、網路連線和網路資源。</span><span class="sxs-lookup"><span data-stu-id="cda86-109">This isolates the application from accessing hardware, files, registry, other applications, network connectivity, and network resources without specific permission.</span></span> <span data-ttu-id="cda86-110">個別資源可能會被設為目標，而不會公開其他資源。</span><span class="sxs-lookup"><span data-stu-id="cda86-110">Individual resources may be targeted without exposing other resources.</span></span> <span data-ttu-id="cda86-111">此外，使用者身分識別會使用屬於使用者串連的唯一身分識別進行保護，而應用程式則會使用最低許可權模型來授與資源。</span><span class="sxs-lookup"><span data-stu-id="cda86-111">Additionally, user identity is protected by using a unique identity that is a concatenation of the user and the app and resources are granted using a least-privilege model.</span></span> <span data-ttu-id="cda86-112">這可進一步防止應用程式模擬使用者，以取得其他資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="cda86-112">This further protects against an app impersonating the user to gain access to other resources.</span></span>

<span data-ttu-id="cda86-113">如需針對繼承應用程式使用 AppContainer 的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="cda86-113">For more information about using AppContainer for Legacy Applications, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cda86-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="cda86-114">In this section</span></span>



| <span data-ttu-id="cda86-115">主題</span><span class="sxs-lookup"><span data-stu-id="cda86-115">Topic</span></span>                                                                       | <span data-ttu-id="cda86-116">描述</span><span class="sxs-lookup"><span data-stu-id="cda86-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cda86-117">AppContainer 隔離</span><span class="sxs-lookup"><span data-stu-id="cda86-117">AppContainer Isolation</span></span>](appcontainer-isolation.md)<br/>             | <span data-ttu-id="cda86-118">隔離是 AppContainer 執行環境的主要目標。</span><span class="sxs-lookup"><span data-stu-id="cda86-118">Isolation is the primary goal of an AppContainer execution environment.</span></span> <span data-ttu-id="cda86-119">藉由將應用程式與不需要的資源和其他應用程式隔離，可將惡意操作的機會降到最低。</span><span class="sxs-lookup"><span data-stu-id="cda86-119">By isolating an application from unneeded resources and other applications, opportunities for malicious manipulation are minimized.</span></span> <span data-ttu-id="cda86-120">根據最低許可權授與存取權，可防止應用程式和使用者存取其權利以外的資源。</span><span class="sxs-lookup"><span data-stu-id="cda86-120">Granting access based upon least-privilege prevents applications and users from accessing resources beyond their rights.</span></span> <span data-ttu-id="cda86-121">控制資源的存取可保護進程、裝置和網路。</span><span class="sxs-lookup"><span data-stu-id="cda86-121">Controlling access to resources protects the process, the device, and the network.</span></span><br/> |
| [<span data-ttu-id="cda86-122">執行 AppContainer</span><span class="sxs-lookup"><span data-stu-id="cda86-122">Implementing an AppContainer</span></span>](implementing-an-appcontainer.md)<br/> | <span data-ttu-id="cda86-123">AppContainer 的執行方式是將新的資訊新增至處理常式權杖、變更 [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) ，讓所有舊版、未修改的存取控制清單 (ACL) 物件預設會封鎖來自 AppContainer 進程的存取要求，以及可供 AppContainers 使用的重新 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="cda86-123">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span><br/>                                                                                        |



 

 

