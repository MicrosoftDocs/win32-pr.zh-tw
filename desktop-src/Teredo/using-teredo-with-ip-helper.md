---
title: 使用 Teredo 搭配 IP Helper
description: 網際網路通訊協定協助程式 (IP 協助程式) API 是由應用程式使用，以收集和提供有關本機電腦網路設定的重要資訊。
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682652"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="e56fb-103">使用 Teredo 搭配 IP Helper</span><span class="sxs-lookup"><span data-stu-id="e56fb-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="e56fb-104">應用程式會使用 [網際網路通訊協定](/windows/desktop/IpHlp/about-ip-helper) 協助程式 (IP 協助程式) API 來收集和提供有關本機電腦網路設定的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="e56fb-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="e56fb-105">在 Windows Vista 平臺上操作時，此資訊會包含指派給 Teredo 介面的動態 UDP 通訊埠，以及可能會發生在指定埠上的變更。</span><span class="sxs-lookup"><span data-stu-id="e56fb-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="e56fb-106">IP 協助程式 API 會利用下列函式來加速使用 Teredo 介面：</span><span class="sxs-lookup"><span data-stu-id="e56fb-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="e56fb-107">**GetTeredoPort**</span><span class="sxs-lookup"><span data-stu-id="e56fb-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="e56fb-108">**NotifyTeredoPortChange**</span><span class="sxs-lookup"><span data-stu-id="e56fb-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="e56fb-109">**NotifyStableUnicastIpAddressTable**</span><span class="sxs-lookup"><span data-stu-id="e56fb-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 