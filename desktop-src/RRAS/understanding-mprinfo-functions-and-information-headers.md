---
title: 瞭解 MprInfo 函式和資訊標頭
description: 下列函式會要求呼叫端傳遞資訊結構或標頭做為其中一個參數。
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932277"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="a687f-103">瞭解 MprInfo 函式和資訊標頭</span><span class="sxs-lookup"><span data-stu-id="a687f-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="a687f-104">下列函式會要求呼叫端傳遞資訊結構或 *標頭* 做為其中一個參數。</span><span class="sxs-lookup"><span data-stu-id="a687f-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="a687f-105">管理功能</span><span class="sxs-lookup"><span data-stu-id="a687f-105">Administration function</span></span>                                                        | <span data-ttu-id="a687f-106">Configuration 函數</span><span class="sxs-lookup"><span data-stu-id="a687f-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a687f-107">沒有管理功能</span><span class="sxs-lookup"><span data-stu-id="a687f-107">No administration function</span></span>                                                     | [<span data-ttu-id="a687f-108">**MprConfigTransportCreate**</span><span class="sxs-lookup"><span data-stu-id="a687f-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="a687f-109">**MprAdminTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="a687f-110">**MprConfigTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="a687f-111">**MprAdminInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="a687f-112">**MprConfigInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="a687f-113">**MprAdminInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="a687f-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="a687f-114">**MprConfigInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="a687f-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="a687f-115">同樣地，下列函數會傳回信息標頭。</span><span class="sxs-lookup"><span data-stu-id="a687f-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="a687f-116">管理功能</span><span class="sxs-lookup"><span data-stu-id="a687f-116">Administration function</span></span>                                                        | <span data-ttu-id="a687f-117">Configuration 函數</span><span class="sxs-lookup"><span data-stu-id="a687f-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="a687f-118">**MprAdminTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="a687f-119">**MprConfigTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="a687f-120">**MprAdminInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="a687f-121">**MprConfigInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a687f-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="a687f-122">針對傳輸函式，資訊標頭包含傳輸的全域資訊。</span><span class="sxs-lookup"><span data-stu-id="a687f-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="a687f-123">針對 (InterfaceTransport) 函式的用戶端，標頭包含用戶端特定的資訊 (例如，正在管理的 OSPF) 。</span><span class="sxs-lookup"><span data-stu-id="a687f-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="a687f-124">資訊標頭和其內容只能使用 [MprInfo](router-information-functions.md) 函式來操作。</span><span class="sxs-lookup"><span data-stu-id="a687f-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="a687f-125">開發人員不應該嘗試直接操作資訊標頭的內容。</span><span class="sxs-lookup"><span data-stu-id="a687f-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="a687f-126">僅介面函式（例如 [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) ）不需要使用 MprInfo 函式。</span><span class="sxs-lookup"><span data-stu-id="a687f-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="a687f-127">使用這些函式傳遞和傳回的資訊一律採用 [**MPR \_ 介面**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) 結構的形式。</span><span class="sxs-lookup"><span data-stu-id="a687f-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 




