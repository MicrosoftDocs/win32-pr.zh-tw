---
description: 系統會使用設定資訊來判斷如何啟動此服務。
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: 服務組態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511209"
---
# <a name="service-configuration"></a><span data-ttu-id="b057a-103">服務組態</span><span class="sxs-lookup"><span data-stu-id="b057a-103">Service Configuration</span></span>

<span data-ttu-id="b057a-104">系統會使用設定資訊來判斷如何啟動此服務。</span><span class="sxs-lookup"><span data-stu-id="b057a-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="b057a-105">設定資訊也包含服務顯示名稱及其描述。</span><span class="sxs-lookup"><span data-stu-id="b057a-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="b057a-106">例如，針對 DHCP 服務，您可以使用「動態主機設定通訊協定服務」顯示名稱，以及「為您網路上的電腦提供網際網路位址」描述。</span><span class="sxs-lookup"><span data-stu-id="b057a-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="b057a-107">若要修改服務物件的設定資訊，設定程式會使用 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) 或 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函數。</span><span class="sxs-lookup"><span data-stu-id="b057a-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="b057a-108">如需範例，請參閱 [變更服務](changing-a-service-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="b057a-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="b057a-109">為了取得服務物件的設定資訊，設定程式會使用 [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) 或 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) 函數。</span><span class="sxs-lookup"><span data-stu-id="b057a-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="b057a-110">如需範例，請參閱 [查詢服務的](querying-a-service-s-configuration.md)設定。</span><span class="sxs-lookup"><span data-stu-id="b057a-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="b057a-111">[**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)和 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)服務設定函數支援使用觸發程式來控制服務啟動。</span><span class="sxs-lookup"><span data-stu-id="b057a-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="b057a-112">若要修改 SCManager 物件或服務物件的安全描述項，設定程式會使用 [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) 函數。</span><span class="sxs-lookup"><span data-stu-id="b057a-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="b057a-113">為了取得安全描述項的複本，設定程式會使用 [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) 函數。</span><span class="sxs-lookup"><span data-stu-id="b057a-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b057a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="b057a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b057a-115">使用 SC 設定服務</span><span class="sxs-lookup"><span data-stu-id="b057a-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
