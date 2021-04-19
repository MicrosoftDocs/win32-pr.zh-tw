---
description: 電話物件是代表實際電話裝置及其所有控制項的實體。
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: 電話物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981188"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="2b1ff-103">電話物件介面</span><span class="sxs-lookup"><span data-stu-id="2b1ff-103">Phone Object Interfaces</span></span>

<span data-ttu-id="2b1ff-104">電話物件是代表實際電話裝置及其所有控制項的實體。</span><span class="sxs-lookup"><span data-stu-id="2b1ff-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="2b1ff-105">[**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)和 [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)介面不會直接在 Phone 物件上公開，但與其緊密相關，並在此處列出以方便參考。</span><span class="sxs-lookup"><span data-stu-id="2b1ff-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="2b1ff-106">介面</span><span class="sxs-lookup"><span data-stu-id="2b1ff-106">Interface</span></span>                                                  | <span data-ttu-id="2b1ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="2b1ff-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b1ff-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="2b1ff-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="2b1ff-109">允許存取電話裝置，其層級可與 TAPI 2 所提供的相同。*x* C API。</span><span class="sxs-lookup"><span data-stu-id="2b1ff-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="2b1ff-110">**ITAutomatedPhoneControl**</span><span class="sxs-lookup"><span data-stu-id="2b1ff-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="2b1ff-111">提供的方法可讓您自動控制手機的聲音和環形，以及根據手機的 hookswitch 狀態進行自動通話處理。</span><span class="sxs-lookup"><span data-stu-id="2b1ff-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="2b1ff-112">**ITPhoneEvent**</span><span class="sxs-lookup"><span data-stu-id="2b1ff-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="2b1ff-113">抓取電話事件的描述。</span><span class="sxs-lookup"><span data-stu-id="2b1ff-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="2b1ff-114">**IEnumPhone**</span><span class="sxs-lookup"><span data-stu-id="2b1ff-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="2b1ff-115">列舉 [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)。</span><span class="sxs-lookup"><span data-stu-id="2b1ff-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



