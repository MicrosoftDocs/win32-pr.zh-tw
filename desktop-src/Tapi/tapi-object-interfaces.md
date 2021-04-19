---
description: TAPI 物件是 TAPI 3 的主要物件。
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: TAPI 物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987298"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="f809c-103">TAPI 物件介面</span><span class="sxs-lookup"><span data-stu-id="f809c-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="f809c-104">[Tapi 物件](tapi-object.md)是 tapi 3 的主要物件。</span><span class="sxs-lookup"><span data-stu-id="f809c-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="f809c-105">[**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)介面不會直接在 TAPI 物件上公開，但與其緊密相關，並在此處列出以供參考之用。</span><span class="sxs-lookup"><span data-stu-id="f809c-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="f809c-106">介面</span><span class="sxs-lookup"><span data-stu-id="f809c-106">Interfaces</span></span>                                                 | <span data-ttu-id="f809c-107">Description</span><span class="sxs-lookup"><span data-stu-id="f809c-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f809c-108">**ITTAPI**</span><span class="sxs-lookup"><span data-stu-id="f809c-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="f809c-109">主要 TAPI 3 介面。</span><span class="sxs-lookup"><span data-stu-id="f809c-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="f809c-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="f809c-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="f809c-111">衍生自 [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi);提供支援電話裝置的其他方法。</span><span class="sxs-lookup"><span data-stu-id="f809c-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="f809c-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="f809c-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="f809c-113">輸出介面，用來接收有關 TAPI 3 事件的非同步資訊。</span><span class="sxs-lookup"><span data-stu-id="f809c-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="f809c-114">**ITTAPICallCenter**</span><span class="sxs-lookup"><span data-stu-id="f809c-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="f809c-115">將輸入介面提供給撥入中心控制項。</span><span class="sxs-lookup"><span data-stu-id="f809c-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="f809c-116">**ITTAPIObjectEvent**</span><span class="sxs-lookup"><span data-stu-id="f809c-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="f809c-117">提供方法來取得有關 TAPI 物件事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="f809c-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="f809c-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="f809c-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="f809c-119">擴充 [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent);提供方法，以抓取造成 TAPI 物件事件的電話物件指標。</span><span class="sxs-lookup"><span data-stu-id="f809c-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
