---
description: CRM 元件可以安裝在 COM + 伺服器應用程式或 COM + 程式庫應用程式中。
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: 設定 COM + CRM 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997071"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="e11c5-103">設定 COM + CRM 元件</span><span class="sxs-lookup"><span data-stu-id="e11c5-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="e11c5-104">CRM 元件可以安裝在 COM + 伺服器應用程式或 COM + 程式庫應用程式中。</span><span class="sxs-lookup"><span data-stu-id="e11c5-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="e11c5-105">不過，它們一定要在 COM + 伺服器應用程式中執行。</span><span class="sxs-lookup"><span data-stu-id="e11c5-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="e11c5-106">如果它們是安裝在 COM + 程式庫應用程式中，就無法在用戶端進程中使用。</span><span class="sxs-lookup"><span data-stu-id="e11c5-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="e11c5-107">如果 CRM 元件是安裝在程式庫應用程式中，則可供多個伺服器應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="e11c5-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="e11c5-108">如果安裝在特定的伺服器應用程式中，則只有該特定伺服器應用程式才能使用這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="e11c5-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="e11c5-109">若要在伺服器應用程式中啟用 CRM 的使用，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="e11c5-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="e11c5-110">在 [元件服務] 的 [伺服器應用程式屬性] 頁面底下，按一下 [ **Advanced** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="e11c5-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="e11c5-111">針對該伺服器應用程式，選取 [ **啟用補償資源管理員** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="e11c5-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="e11c5-112">如果未選取此選項，在此伺服器應用程式中嘗試使用 CRM 的嘗試將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e11c5-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="e11c5-113">如果安裝在程式庫應用程式中，則不需要針對該程式庫應用程式選取 [ **啟用補償資源管理員** ] 選項，但是必須針對要執行 CRM 的伺服器應用程式選取這個選項。</span><span class="sxs-lookup"><span data-stu-id="e11c5-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="e11c5-114">建議您在相同的應用程式中安裝特定 CRM 的 CRM 工作者和 CRM 補償器元件。</span><span class="sxs-lookup"><span data-stu-id="e11c5-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="e11c5-115">CRM 元件的建議設定如下所示。</span><span class="sxs-lookup"><span data-stu-id="e11c5-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="e11c5-116">元件</span><span class="sxs-lookup"><span data-stu-id="e11c5-116">Component</span></span>           | <span data-ttu-id="e11c5-117">設定</span><span class="sxs-lookup"><span data-stu-id="e11c5-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11c5-118">**CRM 背景工作**</span><span class="sxs-lookup"><span data-stu-id="e11c5-118">**CRM Worker**</span></span>      | <span data-ttu-id="e11c5-119">transaction = requiredsync = yesJIT = yesthreading model = (或執行緒模型 = 公寓) </span><span class="sxs-lookup"><span data-stu-id="e11c5-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="e11c5-120">**CRM 補償器**</span><span class="sxs-lookup"><span data-stu-id="e11c5-120">**CRM Compensator**</span></span> | <span data-ttu-id="e11c5-121">transaction = disabledsync = disabledJIT = nothreading model = (或執行緒模型 = 公寓) </span><span class="sxs-lookup"><span data-stu-id="e11c5-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="e11c5-122">使用 CRM 的元件必須在註冊時明確指定執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="e11c5-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="e11c5-123">不支援預設的「主要執行緒單元」。</span><span class="sxs-lookup"><span data-stu-id="e11c5-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="e11c5-124">唯一支援的兩個執行緒模型為「單元」和「兩者」。</span><span class="sxs-lookup"><span data-stu-id="e11c5-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e11c5-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e11c5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e11c5-126">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="e11c5-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



