---
title: 套用至參數的方向屬性
description: 方向屬性 \ in \ 和 out \ 決定用戶端和伺服器如何配置和釋放記憶體。 下表摘要說明雙向屬性對記憶體配置的影響。
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966881"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="4886d-104">套用至參數的方向屬性</span><span class="sxs-lookup"><span data-stu-id="4886d-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="4886d-105">和輸出中的方向屬性會 \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] 決定用戶端和伺服器如何配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4886d-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="4886d-106">下表摘要說明雙向屬性對記憶體配置的影響。</span><span class="sxs-lookup"><span data-stu-id="4886d-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="4886d-107">方向屬性</span><span class="sxs-lookup"><span data-stu-id="4886d-107">Directional attribute</span></span>    | <span data-ttu-id="4886d-108">用戶端上的記憶體</span><span class="sxs-lookup"><span data-stu-id="4886d-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="4886d-109">伺服器上的記憶體</span><span class="sxs-lookup"><span data-stu-id="4886d-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4886d-110">\[[in](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="4886d-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="4886d-111">用戶端應用程式必須在呼叫之前配置。</span><span class="sxs-lookup"><span data-stu-id="4886d-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="4886d-112">伺服器 stub 會配置。</span><span class="sxs-lookup"><span data-stu-id="4886d-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="4886d-113">\[[out](/windows/desktop/Midl/out-idl)\]</span><span class="sxs-lookup"><span data-stu-id="4886d-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="4886d-114">用戶端 stub 會在傳回時配置。</span><span class="sxs-lookup"><span data-stu-id="4886d-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="4886d-115">伺服器 stub 只會配置最上層指標;伺服器應用程式必須配置所有內嵌指標。</span><span class="sxs-lookup"><span data-stu-id="4886d-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="4886d-116">伺服器也會視需要配置新的資料。</span><span class="sxs-lookup"><span data-stu-id="4886d-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="4886d-117">\[**in**、 **out**\]</span><span class="sxs-lookup"><span data-stu-id="4886d-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="4886d-118">用戶端應用程式必須配置傳送至伺服器的初始資料;用戶端 stub 會配置額外的資料。</span><span class="sxs-lookup"><span data-stu-id="4886d-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="4886d-119">伺服器 stub 會配置從用戶端傳輸的初始資料;伺服器應用程式會視需要配置新的資料。</span><span class="sxs-lookup"><span data-stu-id="4886d-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="4886d-120">在上述所有情況下，用戶端 stub 都不會釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4886d-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="4886d-121">用戶端應用程式必須在記憶體終止之前釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4886d-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="4886d-122">當遠端程序呼叫傳回 (受制于 \[ [配置](/windows/desktop/Midl/allocate) \] ACF 屬性) 時，伺服器 stub 會釋出記憶體。</span><span class="sxs-lookup"><span data-stu-id="4886d-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 