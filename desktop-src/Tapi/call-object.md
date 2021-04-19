---
description: 呼叫物件代表本機位址與一或多個其他位址之間的位址連接。
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: 呼叫物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980097"
---
# <a name="call-object"></a><span data-ttu-id="b2a6c-103">呼叫物件</span><span class="sxs-lookup"><span data-stu-id="b2a6c-103">Call Object</span></span>

<span data-ttu-id="b2a6c-104">呼叫物件代表位址在本機位址與一或多個其他位址之間的連接。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="b2a6c-105">所有呼叫控制都是透過呼叫物件來完成。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-105">All call control is done through the Call object.</span></span> <span data-ttu-id="b2a6c-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) 和 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 是呼叫物件上最常使用的介面。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="b2a6c-107">這些介面會執行各種不同的作業和查詢，例如取得媒體資料流程的介面指標或取得呼叫者識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="b2a6c-108">請參閱有關 [會話作業](session-operations-ovr.md) 和 [會話資訊](session-information-ovr.md) 的主要總覽章節，以查看 TAPI 所支援的作業。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="b2a6c-109">媒體服務提供者可以執行由 TAPI 在呼叫物件上匯總的 [提供者特定介面](provider-specific-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="b2a6c-110">如需提供者所執行之功能的詳細資訊，請參閱服務提供者的檔。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="b2a6c-111">[進行呼叫](make-a-call.md)和[接收呼叫](receive-a-call.md)程式碼範例會顯示使用呼叫物件的一些圖例。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="b2a6c-112">請參閱 [呼叫物件介面](call-object-interfaces.md) ，以取得與呼叫物件相關聯之所有介面的清單。</span><span class="sxs-lookup"><span data-stu-id="b2a6c-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



