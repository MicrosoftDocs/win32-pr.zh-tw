---
title: MDM 註冊功能
description: MDM 註冊會使用下列功能。
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316609"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="44450-103">MDM 註冊功能</span><span class="sxs-lookup"><span data-stu-id="44450-103">MDM Registration Functions</span></span>

<span data-ttu-id="44450-104">MDM 註冊會使用下列功能。</span><span class="sxs-lookup"><span data-stu-id="44450-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="44450-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="44450-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="44450-106">**DiscoverManagementService**</span><span class="sxs-lookup"><span data-stu-id="44450-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="44450-107">探索 MDM 服務。</span><span class="sxs-lookup"><span data-stu-id="44450-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-108">**DiscoverManagementServiceEx**</span><span class="sxs-lookup"><span data-stu-id="44450-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="44450-109">使用候選伺服器探索 MDM 服務。</span><span class="sxs-lookup"><span data-stu-id="44450-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-110">**GetDeviceRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="44450-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="44450-111">抓取裝置註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="44450-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-112">**GetManagementAppHyperlink**</span><span class="sxs-lookup"><span data-stu-id="44450-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="44450-113">抓取與 MDM 服務相關聯的管理應用程式超連結。</span><span class="sxs-lookup"><span data-stu-id="44450-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-114">**IsDeviceRegisteredWithManagement**</span><span class="sxs-lookup"><span data-stu-id="44450-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="44450-115">檢查裝置是否已向 MDM 服務註冊。</span><span class="sxs-lookup"><span data-stu-id="44450-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-116">**IsManagementRegistrationAllowed**</span><span class="sxs-lookup"><span data-stu-id="44450-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="44450-117">檢查本機原則是否允許 MDM 註冊。</span><span class="sxs-lookup"><span data-stu-id="44450-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-118">**RegisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="44450-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="44450-119">使用[ \[ MS-MDE \] ：行動裝置註冊通訊協定](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)，向 MDM 服務註冊裝置。</span><span class="sxs-lookup"><span data-stu-id="44450-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="44450-120">**RegisterDeviceWithManagementUsingAADCredentials**</span><span class="sxs-lookup"><span data-stu-id="44450-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="44450-121">使用 Azure Active Directory (AAD) 認證，向 MDM 服務註冊裝置。</span><span class="sxs-lookup"><span data-stu-id="44450-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-122">**SetManagedExternally**</span><span class="sxs-lookup"><span data-stu-id="44450-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="44450-123">向 MDM 代理程式指出裝置是在外部管理的，而且不會向 MDM 服務註冊。</span><span class="sxs-lookup"><span data-stu-id="44450-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="44450-124">**UnregisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="44450-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="44450-125">使用 MDM 服務取消註冊裝置</span><span class="sxs-lookup"><span data-stu-id="44450-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 