---
description: 擴充的電話語音功能會依類別列在下表中。
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: 擴充電話語音服務參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972042"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="279b1-103">擴充電話語音服務參考</span><span class="sxs-lookup"><span data-stu-id="279b1-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="279b1-104">擴充的電話語音功能會依類別列在下表中。</span><span class="sxs-lookup"><span data-stu-id="279b1-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="279b1-105">線路裝置的擴充電話語音功能</span><span class="sxs-lookup"><span data-stu-id="279b1-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="279b1-106">函式</span><span class="sxs-lookup"><span data-stu-id="279b1-106">Function</span></span>                                                   | <span data-ttu-id="279b1-107">描述</span><span class="sxs-lookup"><span data-stu-id="279b1-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="279b1-108">**lineNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="279b1-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="279b1-109">允許應用程式與指定的線路裝置協調使用延伸模組版本。</span><span class="sxs-lookup"><span data-stu-id="279b1-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="279b1-110">非同步：</span><span class="sxs-lookup"><span data-stu-id="279b1-110">Asynchronous.</span></span> |
| [<span data-ttu-id="279b1-111">**lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="279b1-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="279b1-112">提供服務提供者存取其他 TAPI 功能未提供之裝置特定功能的存取權。</span><span class="sxs-lookup"><span data-stu-id="279b1-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="279b1-113">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="279b1-113">Synchronous.</span></span> |
| [<span data-ttu-id="279b1-114">**lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="279b1-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="279b1-115">將裝置特定的交換器功能傳送至交換器。</span><span class="sxs-lookup"><span data-stu-id="279b1-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="279b1-116">非同步：</span><span class="sxs-lookup"><span data-stu-id="279b1-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="279b1-117">電話裝置的擴充電話語音功能</span><span class="sxs-lookup"><span data-stu-id="279b1-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="279b1-118">函式</span><span class="sxs-lookup"><span data-stu-id="279b1-118">Function</span></span>                                                     | <span data-ttu-id="279b1-119">描述</span><span class="sxs-lookup"><span data-stu-id="279b1-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="279b1-120">**phoneDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="279b1-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="279b1-121">裝置特定的 escape 函式，允許廠商相依的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="279b1-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="279b1-122">非同步：</span><span class="sxs-lookup"><span data-stu-id="279b1-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="279b1-123">**PhoneNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="279b1-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="279b1-124">允許應用程式與指定的電話裝置協調使用延伸模組版本。</span><span class="sxs-lookup"><span data-stu-id="279b1-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="279b1-125">Synchronous：</span><span class="sxs-lookup"><span data-stu-id="279b1-125">Synchronous.</span></span> |



 

 

 



