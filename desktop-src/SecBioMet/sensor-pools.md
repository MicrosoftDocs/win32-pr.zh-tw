---
title: 感應器集區
description: 描述三種可能的感應器集區系統、私用和未指派。
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375788"
---
# <a name="sensor-pools"></a><span data-ttu-id="5616d-103">感應器集區</span><span class="sxs-lookup"><span data-stu-id="5616d-103">Sensor Pools</span></span>

<span data-ttu-id="5616d-104">為了支援 Windows 驗證案例和廠商定義的驗證，Windows 生物特徵辨識服務會將生物識別單位組織成三個可能的感應器集區：</span><span class="sxs-lookup"><span data-stu-id="5616d-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="5616d-105">**私** 用集區：配置給用戶端應用程式專用的生物識別單位集合。</span><span class="sxs-lookup"><span data-stu-id="5616d-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="5616d-106">私人集區可支援不是以 Windows 為基礎的驗證案例，而且可讓應用程式以廠商定義的方式存取生物特徵辨識裝置的硬體。</span><span class="sxs-lookup"><span data-stu-id="5616d-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="5616d-107">系統上的私用感應器集區數量可能會和生物識別單位一樣多。</span><span class="sxs-lookup"><span data-stu-id="5616d-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="5616d-108">**系統感應器** 集區可共用的生物特徵辨識單位集合，以提供 Windows 驗證服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="5616d-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="5616d-109">此集區是由 Winlogon、UAC 和任何其他用戶端所使用，這些用戶端會將 SID 與特定生物特徵辨識範本產生關聯。</span><span class="sxs-lookup"><span data-stu-id="5616d-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="5616d-110">每個生物特徵辨識服務提供者都有一個系統感應器集區。</span><span class="sxs-lookup"><span data-stu-id="5616d-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="5616d-111">**未** 指派的集區包含 (可能是未指派給系統集區或私人集區的生物特徵辨識單位) 集合。</span><span class="sxs-lookup"><span data-stu-id="5616d-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="5616d-112">應用程式可以使用共用的系統集區，也可以建立從系統或未指派的集區中移除的生物識別單位所組成的私人集區。</span><span class="sxs-lookup"><span data-stu-id="5616d-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="5616d-113">當應用程式釋放其私人集區時，會重新設定生物特徵辨識單位，並將其傳回至其原創組區。</span><span class="sxs-lookup"><span data-stu-id="5616d-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="5616d-114">為了防止阻絕服務攻擊，只允許具有特殊許可權的使用者從系統集區移除最後一個感應器。</span><span class="sxs-lookup"><span data-stu-id="5616d-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="5616d-115">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="5616d-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5616d-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="5616d-116">In this section</span></span>



| <span data-ttu-id="5616d-117">主題</span><span class="sxs-lookup"><span data-stu-id="5616d-117">Topic</span></span>                                                       | <span data-ttu-id="5616d-118">描述</span><span class="sxs-lookup"><span data-stu-id="5616d-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5616d-119">私人感應器集區</span><span class="sxs-lookup"><span data-stu-id="5616d-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="5616d-120">保留給用戶端應用程式專用使用的生物識別單位集合。</span><span class="sxs-lookup"><span data-stu-id="5616d-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="5616d-121">私人集區支援專屬的驗證方法，並可讓用戶端應用程式使用廠商指定的控制命令來存取生物識別單位。</span><span class="sxs-lookup"><span data-stu-id="5616d-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="5616d-122">系統感應器集區</span><span class="sxs-lookup"><span data-stu-id="5616d-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="5616d-123">可共用的生物識別單位集合，可讓您存取 Windows 驗證服務。</span><span class="sxs-lookup"><span data-stu-id="5616d-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="5616d-124">此集區是由 Winlogon、UAC 和任何其他用戶端所使用，這些用戶端會將 SID 與特定生物特徵辨識範本產生關聯。</span><span class="sxs-lookup"><span data-stu-id="5616d-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="5616d-125">系統集區行為</span><span class="sxs-lookup"><span data-stu-id="5616d-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="5616d-126">討論當事件通知傳送時，以及沒有任何生物特徵辨識作業暫止時，系統集區所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="5616d-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="5616d-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="5616d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5616d-128">關於 Windows 生物特徵辨識架構 API</span><span class="sxs-lookup"><span data-stu-id="5616d-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 

