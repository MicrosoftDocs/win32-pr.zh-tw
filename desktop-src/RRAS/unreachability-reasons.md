---
title: 無法撥號的原因
description: 下表列出表示無法連接介面之原因的常數值。
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023826"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="bddb3-103">無法撥號的原因</span><span class="sxs-lookup"><span data-stu-id="bddb3-103">Unreachability Reasons</span></span>

<span data-ttu-id="bddb3-104">下表列出表示無法連接介面之原因的常數值。</span><span class="sxs-lookup"><span data-stu-id="bddb3-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="bddb3-105">值</span><span class="sxs-lookup"><span data-stu-id="bddb3-105">Value</span></span>                                       | <span data-ttu-id="bddb3-106">意義</span><span class="sxs-lookup"><span data-stu-id="bddb3-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddb3-107">MPR \_ 介面系統 \_ 管理員 \_ 已停用</span><span class="sxs-lookup"><span data-stu-id="bddb3-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="bddb3-108">系統管理員已停用介面。</span><span class="sxs-lookup"><span data-stu-id="bddb3-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="bddb3-109">MPR \_ 介面 \_ 連接 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="bddb3-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="bddb3-110">先前的連接嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="bddb3-110">The previous connection attempt failed.</span></span> <span data-ttu-id="bddb3-111">查看 **dwLastError** 成員中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bddb3-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="bddb3-112">MPR \_ 介面 \_ 撥出時 \_ 數 \_ 限制</span><span class="sxs-lookup"><span data-stu-id="bddb3-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="bddb3-113">目前不允許撥號。</span><span class="sxs-lookup"><span data-stu-id="bddb3-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="bddb3-114">MPR \_ 介面 \_ \_ 資源不足 \_</span><span class="sxs-lookup"><span data-stu-id="bddb3-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="bddb3-115">沒有任何埠或裝置可供使用。</span><span class="sxs-lookup"><span data-stu-id="bddb3-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="bddb3-116">MPR \_ 介面 \_ 服務已 \_ 暫停</span><span class="sxs-lookup"><span data-stu-id="bddb3-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="bddb3-117">暫停服務。</span><span class="sxs-lookup"><span data-stu-id="bddb3-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="bddb3-118">MPR \_ 介面 \_ 無 \_ 媒體 \_ 意義</span><span class="sxs-lookup"><span data-stu-id="bddb3-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="bddb3-119">網路纜線與網路介面卡中斷連線。</span><span class="sxs-lookup"><span data-stu-id="bddb3-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="bddb3-120">MPR \_ 介面 \_ 無 \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="bddb3-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="bddb3-121">網路卡已從電腦移除。</span><span class="sxs-lookup"><span data-stu-id="bddb3-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="bddb3-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="bddb3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bddb3-123">**MPR \_ 介面 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="bddb3-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="bddb3-124">**MPR \_ 介面 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="bddb3-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="bddb3-125">**MIB \_ IFROW**</span><span class="sxs-lookup"><span data-stu-id="bddb3-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="bddb3-126">**MIB \_ IFSTATUS**</span><span class="sxs-lookup"><span data-stu-id="bddb3-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 