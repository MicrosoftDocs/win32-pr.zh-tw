---
title: 多播群組管理員回呼
description: 多播群組管理員會使用下列回呼來通知用戶端 (通常是) 事件和狀態變更的路由通訊協定
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842511"
---
# <a name="multicast-group-manager-callbacks"></a><span data-ttu-id="25650-103">多播群組管理員回呼</span><span class="sxs-lookup"><span data-stu-id="25650-103">Multicast Group Manager Callbacks</span></span>

<span data-ttu-id="25650-104">多播群組管理員會使用下列回呼來通知用戶端 (通常是) 事件和狀態變更的路由通訊協定：</span><span class="sxs-lookup"><span data-stu-id="25650-104">The multicast group manager uses the following callbacks to notify clients (typically, routing protocols) of events and state changes:</span></span>

[<span data-ttu-id="25650-105">**PMGM \_ 建立 \_ 警示 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-105">**PMGM\_CREATION\_ALERT\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[<span data-ttu-id="25650-106">**PMGM \_ 聯結 \_ 警示 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-106">**PMGM\_JOIN\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[<span data-ttu-id="25650-107">**PMGM \_ 剪除 \_ 警示 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-107">**PMGM\_PRUNE\_ALERT\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[<span data-ttu-id="25650-108">**PMGM \_ 本機 \_ 聯結 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-108">**PMGM\_LOCAL\_JOIN\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[<span data-ttu-id="25650-109">**PMGM \_ 本地 \_ 離開 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-109">**PMGM\_LOCAL\_LEAVE\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[<span data-ttu-id="25650-110">**PMGM \_ RPF \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-110">**PMGM\_RPF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[<span data-ttu-id="25650-111">**回呼的 PMGM \_ 錯誤 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="25650-111">**PMGM\_WRONG\_IF\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

<span data-ttu-id="25650-112">多播群組管理員會使用下列回呼來通知 IGMP 事件和狀態變更：</span><span class="sxs-lookup"><span data-stu-id="25650-112">The multicast group manager uses the following callbacks to notify IGMP of events and state changes:</span></span>

[<span data-ttu-id="25650-113">**PMGM \_ 停用 \_ IGMP \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-113">**PMGM\_DISABLE\_IGMP\_CALLBACK**</span></span>](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[<span data-ttu-id="25650-114">**PMGM \_ 啟用 \_ IGMP \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="25650-114">**PMGM\_ENABLE\_IGMP\_CALLBACK**</span></span>](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 