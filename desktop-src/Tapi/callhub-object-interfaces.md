---
description: CallHub 物件會公開方法，以取得有關多方呼叫中參與者的資訊。
ms.assetid: 928c3abb-1b4e-42f3-a8cc-41889ad573ed
title: CallHub 物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe448c7f559d38bef671144c1a6457f43d4a6b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850475"
---
# <a name="callhub-object-interfaces"></a><span data-ttu-id="70cb5-103">CallHub 物件介面</span><span class="sxs-lookup"><span data-stu-id="70cb5-103">CallHub Object Interfaces</span></span>

<span data-ttu-id="70cb5-104">[CallHub 物件](callhub-object.md)會公開方法，以取得有關多方呼叫中參與者的資訊。</span><span class="sxs-lookup"><span data-stu-id="70cb5-104">The [CallHub object](callhub-object.md) exposes methods that retrieve information concerning participants in a multi-party call.</span></span>

<span data-ttu-id="70cb5-105">[**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent)和 [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)介面不會直接在 CallHub 物件上公開，但與其緊密相關，並在此處列出以供參考便利性。</span><span class="sxs-lookup"><span data-stu-id="70cb5-105">The [**ITCallHubEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) and [**IEnumCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub) interfaces are not directly exposed on the CallHub Object, but are tightly related to it and are listed here for reference convenience.</span></span>



| <span data-ttu-id="70cb5-106">介面</span><span class="sxs-lookup"><span data-stu-id="70cb5-106">Interface</span></span>                                | <span data-ttu-id="70cb5-107">描述</span><span class="sxs-lookup"><span data-stu-id="70cb5-107">Description</span></span>                                                           |
|------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="70cb5-108">**ITCallHub**</span><span class="sxs-lookup"><span data-stu-id="70cb5-108">**ITCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)           | <span data-ttu-id="70cb5-109">提供方法來取得有關 CallHub 物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="70cb5-109">Provides methods to retrieve information concerning a CallHub object.</span></span> |
| [<span data-ttu-id="70cb5-110">**ITCallHubEvent**</span><span class="sxs-lookup"><span data-stu-id="70cb5-110">**ITCallHubEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhubevent) | <span data-ttu-id="70cb5-111">用來取得有關 CallHub 事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="70cb5-111">Used to acquire information concerning CallHub events.</span></span>                |
| [<span data-ttu-id="70cb5-112">**IEnumCallHub**</span><span class="sxs-lookup"><span data-stu-id="70cb5-112">**IEnumCallHub**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallhub)     | <span data-ttu-id="70cb5-113">列舉 [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub)。</span><span class="sxs-lookup"><span data-stu-id="70cb5-113">Enumerates [**ITCallHub**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub).</span></span>                            |



 

 

 



