---
description: 無線臨機操作程式設計介面是由下列介面所組成。
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: 無線特定介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982316"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="a3f2f-103">無線特定介面</span><span class="sxs-lookup"><span data-stu-id="a3f2f-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="a3f2f-104">無線臨機操作程式設計介面是由下列介面所組成。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="a3f2f-105">介面名稱</span><span class="sxs-lookup"><span data-stu-id="a3f2f-105">Interface Name</span></span>                                                                       | <span data-ttu-id="a3f2f-106">描述</span><span class="sxs-lookup"><span data-stu-id="a3f2f-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3f2f-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="a3f2f-108">代表 (NIC) 的無線網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="a3f2f-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="a3f2f-110">定義 [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)支援的通知。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="a3f2f-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="a3f2f-112">建立及管理802.11 臨機操作網路。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="a3f2f-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="a3f2f-114">定義 [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) 介面所支援的通知。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="a3f2f-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="a3f2f-116">代表連接範圍內的可用特定網路目的地。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="a3f2f-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="a3f2f-118">定義 [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) 介面所支援的通知。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="a3f2f-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="a3f2f-120">指定無線特定網路的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="a3f2f-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="a3f2f-122">表示目前可見的802.11 特定網路介面集合。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="a3f2f-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="a3f2f-124">表示目前可見的802.11 特定網路集合。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="a3f2f-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="a3f2f-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="a3f2f-126">表示與每個可見無線臨機操作網路相關聯的安全性設定集合。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="a3f2f-127">未來的 Windows 版本可能無法使用臨機操作模式。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="a3f2f-128">從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 [Wi-Fi Direct](about-the-wi-fi-direct-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="a3f2f-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



