---
title: 使用 DNS WMI 提供者的總覽
description: 下列一般步驟可讓您開始建立自己的腳本或使用 DNS WMI 提供者的程式。
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021732"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="b79cd-103">使用 DNS WMI 提供者的總覽</span><span class="sxs-lookup"><span data-stu-id="b79cd-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="b79cd-104">下列一般步驟可讓您開始建立自己的腳本或使用 DNS WMI 提供者的程式。</span><span class="sxs-lookup"><span data-stu-id="b79cd-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="b79cd-105">**使用 DNS WMI 提供者建立腳本或程式**</span><span class="sxs-lookup"><span data-stu-id="b79cd-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="b79cd-106">連接到 DNS WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="b79cd-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="b79cd-107">DNS WMI 提供者的命名空間一律會是 "root \\ microsoftdns"。</span><span class="sxs-lookup"><span data-stu-id="b79cd-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="b79cd-108">取得 DNS 伺服器實例。</span><span class="sxs-lookup"><span data-stu-id="b79cd-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="b79cd-109">根據您想要執行的型別動作，取得 DNS 區域或記錄實例。</span><span class="sxs-lookup"><span data-stu-id="b79cd-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="b79cd-110">執行想要的動作：</span><span class="sxs-lookup"><span data-stu-id="b79cd-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="b79cd-111">執行方法</span><span class="sxs-lookup"><span data-stu-id="b79cd-111">Execute a method</span></span>
    -   <span data-ttu-id="b79cd-112">顯示內容</span><span class="sxs-lookup"><span data-stu-id="b79cd-112">Display a property</span></span>
    -   <span data-ttu-id="b79cd-113">修改屬性 (必須有讀取/寫入存取權) </span><span class="sxs-lookup"><span data-stu-id="b79cd-113">Modify a property (must have Read/Write access)</span></span>

 

 




