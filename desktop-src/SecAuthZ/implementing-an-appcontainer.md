---
description: AppContainer 的執行方式是將新的資訊新增至處理常式權杖、變更 SeAccessCheck () ，讓所有舊版、未修改的存取控制清單 (ACL) 物件預設會封鎖來自 AppContainer 進程的存取要求，以及可供 AppContainers 使用的重新 ACL 物件。
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: 執行 AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851695"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="c0b4e-103">執行 AppContainer</span><span class="sxs-lookup"><span data-stu-id="c0b4e-103">Implementing an AppContainer</span></span>

<span data-ttu-id="c0b4e-104">AppContainer 的執行方式是將新的資訊新增至處理常式權杖、變更 [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) ，讓所有舊版、未修改的存取控制清單 (ACL) 物件預設會封鎖來自 AppContainer 進程的存取要求，以及可供 AppContainers 使用的重新 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="c0b4e-105">程序</span><span class="sxs-lookup"><span data-stu-id="c0b4e-105">The process</span></span>

<span data-ttu-id="c0b4e-106">首先，新增處理常式權杖的新資訊。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="c0b4e-107">然後變更 **SeAccessCheck ()** ，如此一來，所有舊版、未修改的 acl 預設將會封鎖來自 AppContainer 進程的存取要求。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="c0b4e-108">最後，應可供 AppContainers 的重新 ACL 資源</span><span class="sxs-lookup"><span data-stu-id="c0b4e-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="c0b4e-109">AppContainer SID 是 appcontainer 的持續性唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="c0b4e-110">功能 Sid 會將資源群組的存取權授與 AppContainers 群組。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="c0b4e-111">AppContainerNumber 是用來區別 AppContainers 的暫時性 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="c0b4e-112">不過，它不應該用來作為 AppContainer 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="c0b4e-113">若要允許單一 AppContainer 存取資源，請將其 AppContainerSID 新增至該資源的 ACL。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="c0b4e-114">若要允許數個特定 AppContainers 存取資源，請將其所有 AppContainerSIDs 新增至該資源的 ACL。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="c0b4e-115">若要管理許可權群組，請建立 (GUID) 的功能 SID，並將該功能 SID 放在要授與的所有資源上。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="c0b4e-116">然後將功能 SID 新增至您的進程權杖。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="c0b4e-117">若要允許所有 AppContainers 存取資源，請將 **所有應用程式封裝** SID 新增至該資源的 ACL。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="c0b4e-118">這相當於萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-118">This acts like a wildcard.</span></span>

<span data-ttu-id="c0b4e-119">AppContainerSID 和 CapabilitySID 都支援存取控制專案 (ACE) 的存取遮罩。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="c0b4e-120">適當設定。</span><span class="sxs-lookup"><span data-stu-id="c0b4e-120">Set as appropriate.</span></span>

 

 
