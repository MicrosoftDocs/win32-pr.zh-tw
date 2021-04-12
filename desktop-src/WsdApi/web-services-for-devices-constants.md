---
description: 裝置上的 Web 服務會使用下列常數。
ms.assetid: ef3df24a-46a1-49de-b2f7-bfccdc793462
title: '裝置上的 Web 服務常數 (Wsdutil .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984946df757e059ef667b94274818aa2b38c87f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192902"
---
# <a name="web-services-on-devices-constants"></a><span data-ttu-id="fc7b0-103">裝置上的 Web 服務常數</span><span class="sxs-lookup"><span data-stu-id="fc7b0-103">Web Services on Devices Constants</span></span>

<span data-ttu-id="fc7b0-104">裝置上的 Web 服務會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="fc7b0-104">The following constants are used by Web Services on Devices.</span></span>



| <span data-ttu-id="fc7b0-105">常數</span><span class="sxs-lookup"><span data-stu-id="fc7b0-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="fc7b0-106">描述</span><span class="sxs-lookup"><span data-stu-id="fc7b0-106">Description</span></span>                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WSD_DEFAULT_HOSTING_ADDRESS"></span><span id="wsd_default_hosting_address"></span><dl> <span data-ttu-id="fc7b0-107"><dt>**WSD \_ 預設 \_ 主機 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="fc7b0-107"><dt>**WSD\_DEFAULT\_HOSTING\_ADDRESS**</dt></span></span> </dl>                       | <span data-ttu-id="fc7b0-108">預設位址 ([UrlPrefix](/windows/desktop/Http/urlprefix-strings) 格式) ，WSDAPI 主機會使用此格式接聽埠5357上的要求。</span><span class="sxs-lookup"><span data-stu-id="fc7b0-108">The default address (in [UrlPrefix](/windows/desktop/Http/urlprefix-strings) format) that a WSDAPI host will use to listen for requests on port 5357.</span></span> <br/>                                                 |
| <span id="WSD_DEFAULT_SECURE_HOSTING_ADDRESS"></span><span id="wsd_default_secure_hosting_address"></span><dl> <span data-ttu-id="fc7b0-109"><dt>**WSD \_ 預設 \_ 安全 \_ 裝載 \_ 位址**</dt></span><span class="sxs-lookup"><span data-stu-id="fc7b0-109"><dt>**WSD\_DEFAULT\_SECURE\_HOSTING\_ADDRESS**</dt></span></span> </dl> | <span data-ttu-id="fc7b0-110">預設安全位址 (為 [UrlPrefix](/windows/desktop/Http/urlprefix-strings) 格式) ，WSDAPI 主機會使用此格式接聽埠5358上的要求。</span><span class="sxs-lookup"><span data-stu-id="fc7b0-110">The default secure address (in [UrlPrefix](/windows/desktop/Http/urlprefix-strings) format) that a WSDAPI host will use to listen for requests on port 5358.</span></span> <br/>                                          |
| <span id="WSD_DEFAULT_EVENTING_ADDRESS__"></span><span id="wsd_default_eventing_address__"></span><dl> <span data-ttu-id="fc7b0-111"><dt>**WSD \_預設 \_ 事件 \_ 處理位址**</dt></span><span class="sxs-lookup"><span data-stu-id="fc7b0-111"><dt>**WSD\_DEFAULT\_EVENTING\_ADDRESS** </dt></span></span> </dl>               | <span data-ttu-id="fc7b0-112">預設位址 (為 [UrlPrefix](/windows/desktop/Http/urlprefix-strings) 格式) ，WSDAPI 主機會使用此格式來接聽埠5358上的安全主機和埠5357上的事件（適用于其他主機）。</span><span class="sxs-lookup"><span data-stu-id="fc7b0-112">The default address (in [UrlPrefix](/windows/desktop/Http/urlprefix-strings) format) that a WSDAPI host will use to listen for events on port 5358 for secure hosts and on port 5357 for other hosts.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="fc7b0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc7b0-113">Requirements</span></span>



| <span data-ttu-id="fc7b0-114">需求</span><span class="sxs-lookup"><span data-stu-id="fc7b0-114">Requirement</span></span> | <span data-ttu-id="fc7b0-115">值</span><span class="sxs-lookup"><span data-stu-id="fc7b0-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7b0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc7b0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7b0-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc7b0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fc7b0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc7b0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7b0-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc7b0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fc7b0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fc7b0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7b0-121"><dt>Wsdutil。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc7b0-121"><dt>Wsdutil.h</dt></span></span> </dl> |



 

