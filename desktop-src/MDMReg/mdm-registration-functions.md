---
title: MDM 註冊功能
description: 下列函式會在中宣告 `mdmregistration.h` ，並由 MDM 註冊使用。
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: 2ca04c3c28f3de289bad6f06feaab0aff9ef2909
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550553"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="efa31-103">MDM 註冊功能</span><span class="sxs-lookup"><span data-stu-id="efa31-103">MDM registration functions</span></span>

<span data-ttu-id="efa31-104">下列函式會在中宣告 `mdmregistration.h` ，並由 MDM 註冊使用。</span><span class="sxs-lookup"><span data-stu-id="efa31-104">The following functions are declared in `mdmregistration.h`, and are used by MDM registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="efa31-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="efa31-105">In this section</span></span>

| <span data-ttu-id="efa31-106">主題</span><span class="sxs-lookup"><span data-stu-id="efa31-106">Topic</span></span> | <span data-ttu-id="efa31-107">描述</span><span class="sxs-lookup"><span data-stu-id="efa31-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="efa31-108">**DiscoverManagementService**</span><span class="sxs-lookup"><span data-stu-id="efa31-108">**DiscoverManagementService**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | <span data-ttu-id="efa31-109">探索 MDM 服務。</span><span class="sxs-lookup"><span data-stu-id="efa31-109">Discovers the MDM service.</span></span> |
| [<span data-ttu-id="efa31-110">**DiscoverManagementServiceEx**</span><span class="sxs-lookup"><span data-stu-id="efa31-110">**DiscoverManagementServiceEx**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | <span data-ttu-id="efa31-111">使用候選伺服器探索 MDM 服務。</span><span class="sxs-lookup"><span data-stu-id="efa31-111">Discovers the MDM service using a candidate server.</span></span> |
| [<span data-ttu-id="efa31-112">**GetDeviceManagementConfigInfo**</span><span class="sxs-lookup"><span data-stu-id="efa31-112">**GetDeviceManagementConfigInfo**</span></span>](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | <span data-ttu-id="efa31-113">取得與提供者識別碼相關聯的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="efa31-113">Gets the config info associated with the provider ID.</span></span> |
| [<span data-ttu-id="efa31-114">**GetDeviceRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="efa31-114">**GetDeviceRegistrationInfo**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | <span data-ttu-id="efa31-115">抓取裝置註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="efa31-115">Retrieves the device registration information.</span></span> |
| [<span data-ttu-id="efa31-116">**GetManagementAppHyperlink**</span><span class="sxs-lookup"><span data-stu-id="efa31-116">**GetManagementAppHyperlink**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | <span data-ttu-id="efa31-117">抓取與 MDM 服務相關聯的管理應用程式超連結。</span><span class="sxs-lookup"><span data-stu-id="efa31-117">Retrieves the management app hyperlink associated with the MDM service.</span></span> |
| [<span data-ttu-id="efa31-118">**IsDeviceRegisteredWithManagement**</span><span class="sxs-lookup"><span data-stu-id="efa31-118">**IsDeviceRegisteredWithManagement**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | <span data-ttu-id="efa31-119">檢查裝置是否已向 MDM 服務註冊。</span><span class="sxs-lookup"><span data-stu-id="efa31-119">Checks whether the device is registered with an MDM service.</span></span> |
| [<span data-ttu-id="efa31-120">**IsManagementRegistrationAllowed**</span><span class="sxs-lookup"><span data-stu-id="efa31-120">**IsManagementRegistrationAllowed**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | <span data-ttu-id="efa31-121">檢查本機原則是否允許 MDM 註冊。</span><span class="sxs-lookup"><span data-stu-id="efa31-121">Checks whether MDM registration is allowed by local policy.</span></span> |
| [<span data-ttu-id="efa31-122">**RegisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="efa31-122">**RegisterDeviceWithManagement**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | <span data-ttu-id="efa31-123">使用[ \[ MS-MDE \] ：行動裝置註冊通訊協定](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)，向 MDM 服務註冊裝置。</span><span class="sxs-lookup"><span data-stu-id="efa31-123">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span> |
| [<span data-ttu-id="efa31-124">**RegisterDeviceWithManagementUsingAADCredentials**</span><span class="sxs-lookup"><span data-stu-id="efa31-124">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | <span data-ttu-id="efa31-125">使用 Azure Active Directory (AAD) 認證，向 MDM 服務註冊裝置。</span><span class="sxs-lookup"><span data-stu-id="efa31-125">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span> |
| [<span data-ttu-id="efa31-126">**SetDeviceManagementConfigInfo**</span><span class="sxs-lookup"><span data-stu-id="efa31-126">**SetDeviceManagementConfigInfo**</span></span>](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | <span data-ttu-id="efa31-127">設定與提供者識別碼相關聯的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="efa31-127">Sets the config info associated with the provider ID.</span></span> |
| [<span data-ttu-id="efa31-128">**SetManagedExternally**</span><span class="sxs-lookup"><span data-stu-id="efa31-128">**SetManagedExternally**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | <span data-ttu-id="efa31-129">向 MDM 代理程式指出裝置是在外部管理的，而且不會向 MDM 服務註冊。</span><span class="sxs-lookup"><span data-stu-id="efa31-129">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span> |
| [<span data-ttu-id="efa31-130">**UnregisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="efa31-130">**UnregisterDeviceWithManagement**</span></span>](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | <span data-ttu-id="efa31-131">使用 MDM 服務將裝置取消註冊。</span><span class="sxs-lookup"><span data-stu-id="efa31-131">Unregisters a device with the MDM service.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="efa31-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="efa31-132">Related topics</span></span>

* [<span data-ttu-id="efa31-133">MDM 註冊參考</span><span class="sxs-lookup"><span data-stu-id="efa31-133">MDM registration reference</span></span>](./mdm-registration-reference.md)
