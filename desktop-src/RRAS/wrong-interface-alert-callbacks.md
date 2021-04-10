---
title: 錯誤的介面警示回呼
description: 當核心轉寄站接收到來自錯誤介面上特定來源的多播資料之後，它會通知多播群組管理員。
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675475"
---
# <a name="wrong-interface-alert-callbacks"></a><span data-ttu-id="409d1-103">錯誤的介面警示回呼</span><span class="sxs-lookup"><span data-stu-id="409d1-103">Wrong Interface Alert Callbacks</span></span>

<span data-ttu-id="409d1-104">當核心轉寄站接收到來自錯誤介面上特定來源的多播資料之後，它會通知多播群組管理員。</span><span class="sxs-lookup"><span data-stu-id="409d1-104">After the kernel forwarder receives multicast data from a specific source on the wrong interface, it notifies the multicast group manager.</span></span> <span data-ttu-id="409d1-105">[**\_ \_ 如果 \_ 回呼**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)回呼的路由通訊協定擁有資料未正確抵達的介面，則多播群組管理員接著會叫用 PMGM 錯誤。</span><span class="sxs-lookup"><span data-stu-id="409d1-105">The multicast group manager then invokes the [**PMGM\_WRONG\_IF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback to the routing protocol that owns the interface on which the data incorrectly arrived.</span></span>

> [!Note]  
> <span data-ttu-id="409d1-106">這一版的 MGM API 目前未執行此回呼。</span><span class="sxs-lookup"><span data-stu-id="409d1-106">This callback is not currently implemented in this version of the MGM API.</span></span>

 

 

 




