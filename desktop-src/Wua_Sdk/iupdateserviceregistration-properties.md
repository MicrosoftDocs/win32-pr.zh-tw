---
description: IUpdateServiceRegistration 介面會定義下列屬性。
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: IUpdateServiceRegistration 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973415"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="6da69-103">IUpdateServiceRegistration 屬性</span><span class="sxs-lookup"><span data-stu-id="6da69-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="6da69-104">**IUpdateServiceRegistration** 介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6da69-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="6da69-105">屬性</span><span class="sxs-lookup"><span data-stu-id="6da69-105">Property</span></span>                                                                                      | <span data-ttu-id="6da69-106">描述</span><span class="sxs-lookup"><span data-stu-id="6da69-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6da69-107">**IsPendingRegistrationWithAU**</span><span class="sxs-lookup"><span data-stu-id="6da69-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="6da69-108">取得布林值，這個值會指出服務是否也會在新增時向自動更新註冊。</span><span class="sxs-lookup"><span data-stu-id="6da69-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="6da69-109">**>registrationstate**</span><span class="sxs-lookup"><span data-stu-id="6da69-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="6da69-110">取得 [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) 值，這個值表示服務註冊的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6da69-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="6da69-111">**服務**</span><span class="sxs-lookup"><span data-stu-id="6da69-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="6da69-112">取得 [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6da69-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="6da69-113">這個屬性是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="6da69-113">This property is the default property.</span></span>                                    |



 

 

 



