---
description: 陰影複製提供者註冊和載入
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: 陰影複製提供者註冊和載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318976"
---
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="1f6c1-103">陰影複製提供者註冊和載入</span><span class="sxs-lookup"><span data-stu-id="1f6c1-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="1f6c1-104">提供者註冊</span><span class="sxs-lookup"><span data-stu-id="1f6c1-104">Provider Registration</span></span>

<span data-ttu-id="1f6c1-105">只有 VSS 會呼叫提供者。</span><span class="sxs-lookup"><span data-stu-id="1f6c1-105">Only VSS calls providers.</span></span> <span data-ttu-id="1f6c1-106">提供者會藉由叫用 [**IVssAdmin：： RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider)，傳遞 *EProviderType* 參數的 **VSS \_ >prov \_ 硬體** 來註冊呼叫。</span><span class="sxs-lookup"><span data-stu-id="1f6c1-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="1f6c1-107">註冊之後，提供者將會牽涉到陰影複製管理，直到使用 [**IVssAdmin：： UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider)取消註冊為止。</span><span class="sxs-lookup"><span data-stu-id="1f6c1-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="1f6c1-108">提供者載入和卸載</span><span class="sxs-lookup"><span data-stu-id="1f6c1-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="1f6c1-109">提供者可以經常載入和卸載。</span><span class="sxs-lookup"><span data-stu-id="1f6c1-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="1f6c1-110">提供者可以執行 [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) ，以判斷 VSS 載入或卸載提供者的時機。</span><span class="sxs-lookup"><span data-stu-id="1f6c1-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



