---
title: 名稱服務專案的準則
description: 使用遠端程序呼叫 (RPC) 的名稱服務專案準則。
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462313"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="3615f-103">名稱服務專案的準則</span><span class="sxs-lookup"><span data-stu-id="3615f-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="3615f-104">處理名稱服務專案時，會使用下列準則：</span><span class="sxs-lookup"><span data-stu-id="3615f-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="3615f-105">如果您為 [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)提供非 **Null** 的專案名稱，該專案將會是搜尋系結控制碼的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="3615f-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="3615f-106">如果您傳遞 **Null**，則會搜尋登入網域中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="3615f-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="3615f-107">請注意，這不包含受信任的網域。</span><span class="sxs-lookup"><span data-stu-id="3615f-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="3615f-108">如果您提供介面控制碼，只有當專案的介面區段包含該介面 UUID 的相容版本時，才會從專案傳回系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="3615f-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="3615f-109">也就是說，主要版本號碼必須與您的介面 UUID 相同，而次要版本號碼必須等於或大於您的介面。</span><span class="sxs-lookup"><span data-stu-id="3615f-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="3615f-110">如果您提供物件 UUID，則只有當專案的物件 UUID 區段包含該特定物件 UUID 時，才會從專案傳回系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="3615f-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="3615f-111">如果名稱服務專案繼續生存以上所述的準則，則會收集來自這些專案的所有系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="3615f-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="3615f-112">系統會捨棄用戶端不支援的通訊協定順序的控制碼，並將其餘的控制碼傳回給您，作為 [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)的輸出。</span><span class="sxs-lookup"><span data-stu-id="3615f-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




