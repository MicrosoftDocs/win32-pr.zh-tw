---
title: 建立硬體事件訂閱
description: 在已安裝「基礎板管理控制器」 (BMC) 的電腦上，系統事件記錄檔會引發硬體事件並記錄在系統事件記錄檔 (SEL) ，也就是儲存在非動態記憶體的 BMC 事件存放區。
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315916"
---
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="b0b0a-103">建立硬體事件訂閱</span><span class="sxs-lookup"><span data-stu-id="b0b0a-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="b0b0a-104">在已安裝「基礎板管理控制器」 (BMC) 的電腦上，系統事件記錄檔會引發硬體事件並記錄在系統事件記錄檔 (SEL) ，也就是儲存在非動態記憶體的 BMC 事件存放區。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="b0b0a-105">若要使用事件檢視器在 Windows Server 2008 上讀取這些硬體事件，您必須建立事件的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="b0b0a-106">硬體事件訂用帳戶只會在 Windows Server 2008 上運作。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="b0b0a-107">下列程式定義如何建立 SEL 事件訂用帳戶來取出硬體事件：</span><span class="sxs-lookup"><span data-stu-id="b0b0a-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="b0b0a-108">將下列 XML 儲存在 .xml 檔案中 (在此範例中，檔案的名稱 Wsmanselrg.xml) 。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="b0b0a-109">此 XML 會定義訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-109">This XML defines the subscription.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  <span data-ttu-id="b0b0a-110">在命令提示字元視窗中執行下列命令，以建立事件訂用帳戶 (Wecutil.exe 程式位於% SYSTEMROOT% \\ System32 目錄中。 ) ：</span><span class="sxs-lookup"><span data-stu-id="b0b0a-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="b0b0a-111">**>wecutil cs** *<path> \\wsmanselrg.xml*</span><span class="sxs-lookup"><span data-stu-id="b0b0a-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="b0b0a-112">在命令提示字元視窗中執行下列命令，以確定訂用帳戶為使用中狀態：</span><span class="sxs-lookup"><span data-stu-id="b0b0a-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="b0b0a-113">**>wecutil gr** *wsmanselrg*</span><span class="sxs-lookup"><span data-stu-id="b0b0a-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="b0b0a-114">BMC 是在本機與伺服器連接的微控制器。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="b0b0a-115">Bmc 的感應器會監視伺服器的實體狀態，以及可透過網路通訊的個別網路連線（即使伺服器已離線）。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="b0b0a-116">您可以透過智慧型平臺管理介面 (IPMI) WMI 提供者來存取 BMC 資料。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="b0b0a-117">如需有關 IPMI 提供者的詳細資訊，請參閱 [Ipmi 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="b0b0a-118">電腦必須安裝 BMC 和 IPMI 提供者，才能讓事件訂用帳戶運作。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="b0b0a-119">針對在 Windows Server 2008 上執行的電腦，預設會安裝 IPMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="b0b0a-120">如果無法使用 BMC，則無法安裝 IPMI 驅動程式，且訂用帳戶執行時間狀態一律會顯示錯誤 (0x8004001-WMI 一般失敗) 。</span><span class="sxs-lookup"><span data-stu-id="b0b0a-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 