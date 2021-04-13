---
title: 通道繫結
description: 系結會指定通道的有線通訊協定和本機行為。
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Windows 的系結 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301127"
---
# <a name="channel-binding"></a><span data-ttu-id="73005-106">通道繫結</span><span class="sxs-lookup"><span data-stu-id="73005-106">Channel Binding</span></span>

<span data-ttu-id="73005-107">系結會指定通道的有線通訊協定和本機行為。</span><span class="sxs-lookup"><span data-stu-id="73005-107">Bindings specify the wire protocol and local behavior for a channel.</span></span> <span data-ttu-id="73005-108">系結是由下列元件所組成：</span><span class="sxs-lookup"><span data-stu-id="73005-108">Bindings are made up of the following components:</span></span>

-   <span data-ttu-id="73005-109">[**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結，識別要使用的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="73005-109">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use.</span></span>
-   <span data-ttu-id="73005-110">[**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)，指定如何保護通道的安全。</span><span class="sxs-lookup"><span data-stu-id="73005-110">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="73005-111">設定的 [**WS \_ 通道 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s，指定其他選擇性設定 (另請參閱 [**WS \_ 通道 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) 。</span><span class="sxs-lookup"><span data-stu-id="73005-111">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings (see also [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span></span>

 

 




