---
title: 路由器資訊區塊的 IPX 資訊類型
description: 下列資訊類型列在 Ipxrtdef 中。 執行 IPX 傳輸時，請將這些資訊類型與路由器資訊區塊功能搭配使用。
ms.assetid: 6cbc8415-f5ba-4f84-a23f-dd4f4a54d118
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4494da951c04433da2cf9b1da20db7ea5f3119
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023841"
---
# <a name="ipx-information-types-for-router-information-blocks"></a><span data-ttu-id="ff027-104">路由器資訊區塊的 IPX 資訊類型</span><span class="sxs-lookup"><span data-stu-id="ff027-104">IPX Information Types for Router Information Blocks</span></span>

<span data-ttu-id="ff027-105">下列資訊類型列在 Ipxrtdef 中。</span><span class="sxs-lookup"><span data-stu-id="ff027-105">The following information types are listed in Ipxrtdef.h.</span></span> <span data-ttu-id="ff027-106">執行 IPX 傳輸時，請將這些資訊類型與路由器資訊區塊功能搭配使用。</span><span class="sxs-lookup"><span data-stu-id="ff027-106">Use these information types with the router information block functions when running the IPX transport.</span></span>



| <span data-ttu-id="ff027-107">資訊類型</span><span class="sxs-lookup"><span data-stu-id="ff027-107">Information type</span></span>                              | <span data-ttu-id="ff027-108">資訊結構</span><span class="sxs-lookup"><span data-stu-id="ff027-108">Information structure</span></span>                                          |
|-----------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="ff027-109">IPX \_ 介面卡 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-109">IPX\_ADAPTER\_INFO\_TYPE</span></span>                      | <span data-ttu-id="ff027-110">IPX \_ 介面卡 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-110">IPX\_ADAPTER\_INFO</span></span>                                             |
| <span data-ttu-id="ff027-111">IPX \_ 全域 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-111">IPX\_GLOBAL\_INFO\_TYPE</span></span>                       | <span data-ttu-id="ff027-112">IPX \_ 全域 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-112">IPX\_GLOBAL\_INFO</span></span>                                              |
| <span data-ttu-id="ff027-113">IPX \_ 介面 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-113">IPX\_INTERFACE\_INFO\_TYPE</span></span>                    | [<span data-ttu-id="ff027-114">**IPX （ \_ 如果 \_ 資訊）**</span><span class="sxs-lookup"><span data-stu-id="ff027-114">**IPX\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipx_if_info)                           |
| <span data-ttu-id="ff027-115">\_ \_ 流量 \_ 篩選器 \_ 全域 \_ 資訊 \_ 類型中的 IPX</span><span class="sxs-lookup"><span data-stu-id="ff027-115">IPX\_IN\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span>  | <span data-ttu-id="ff027-116">IPX \_ 流量 \_ 篩選 \_ 全域 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-116">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="ff027-117">IPX \_ 輸出 \_ 流量 \_ 篩選 \_ 全域 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-117">IPX\_OUT\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span> | <span data-ttu-id="ff027-118">IPX \_ 流量 \_ 篩選 \_ 全域 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-118">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="ff027-119">\_ \_ 流量 \_ 篩選器 \_ 資訊 \_ 類型中的 IPX</span><span class="sxs-lookup"><span data-stu-id="ff027-119">IPX\_IN\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>          | <span data-ttu-id="ff027-120">IPX \_ 流量 \_ 篩選器 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-120">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="ff027-121">IPX \_ 輸出 \_ 流量 \_ 篩選器 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-121">IPX\_OUT\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>         | <span data-ttu-id="ff027-122">IPX \_ 流量 \_ 篩選器 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-122">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="ff027-123">IPX \_ 靜態 \_ NETBIOS \_ 名稱 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-123">IPX\_STATIC\_NETBIOS\_NAME\_INFO\_TYPE</span></span>        | <span data-ttu-id="ff027-124">IPX \_ 靜態 \_ NETBIOS \_ 名稱 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-124">IPX\_STATIC\_NETBIOS\_NAME\_INFO</span></span>                               |
| <span data-ttu-id="ff027-125">IPX \_ 靜態 \_ 路由 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-125">IPX\_STATIC\_ROUTE\_INFO\_TYPE</span></span>                | <span data-ttu-id="ff027-126">IPX \_ 靜態 \_ 路由 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="ff027-126">IPX\_STATIC\_ROUTE\_INFO</span></span>                                       |
| <span data-ttu-id="ff027-127">IPX \_ 靜態 \_ 服務 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-127">IPX\_STATIC\_SERVICE\_INFO\_TYPE</span></span>              | <span data-ttu-id="ff027-128">[**IPX \_ 靜態 \_ 服務 \_ 資訊**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff027-128">[**IPX\_STATIC\_SERVICE\_INFO**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span></span> |
| <span data-ttu-id="ff027-129">IPXWAN \_ 介面 \_ 資訊 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ff027-129">IPXWAN\_INTERFACE\_INFO\_TYPE</span></span>                 | [<span data-ttu-id="ff027-130">**IPXWAN \_ IF \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="ff027-130">**IPXWAN\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipxwan_if_info)                     |



 

 

 