---
description: 網路封包提供者 (NPPs) 公開 IDelaydC、IESP、IRTC 和 IStats 介面。
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: 選取 NPP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848761"
---
# <a name="selecting-an-npp-interface"></a><span data-ttu-id="99884-103">選取 NPP 介面</span><span class="sxs-lookup"><span data-stu-id="99884-103">Selecting an NPP Interface</span></span>

<span data-ttu-id="99884-104">網路封包提供者 (NPPs) 公開 [**IDelaydC**](idelaydc.md)、 [**IESP**](iesp.md)、 [**IRTC**](irtc.md)和 [**IStats**](istats.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="99884-104">Network packet providers (NPPs) expose the [**IDelaydC**](idelaydc.md), [**IESP**](iesp.md), [**IRTC**](irtc.md), and [**IStats**](istats.md) interfaces.</span></span> <span data-ttu-id="99884-105">這些介面每一個都會提供類似的方法，將 NPP 連接到網路、捕獲網路流量，以及收集有關已捕捉資料的統計資訊。</span><span class="sxs-lookup"><span data-stu-id="99884-105">Each of these interfaces provides similar methods for connecting the NPP to the network, capturing network traffic, and collecting statistical information about the captured data.</span></span> <span data-ttu-id="99884-106">若要選擇要使用的介面，請參閱下表。</span><span class="sxs-lookup"><span data-stu-id="99884-106">To choose which interface to use, refer to the following table.</span></span>

> [!Note]  
> <span data-ttu-id="99884-107">當您使用其中一個介面將 NPP 連接到網路時，您只能使用該介面所提供的方法。</span><span class="sxs-lookup"><span data-stu-id="99884-107">When you connect an NPP to the network with one of these interfaces, you can only use the methods provided by that interface.</span></span> <span data-ttu-id="99884-108">例如，如果您使用 [**IRTC**](irtc.md) 介面連接到網路，然後嘗試使用 [**IDelaydC**](idelaydc.md)啟動捕捉，則啟動捕獲的呼叫將會失敗，而且會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99884-108">For example, if you connect to the network using the [**IRTC**](irtc.md) interface and then try to start a capture with [**IDelaydC**](idelaydc.md), your call to start the capture will fail, and an error code will be returned.</span></span>

 



| <span data-ttu-id="99884-109">介面</span><span class="sxs-lookup"><span data-stu-id="99884-109">Interface</span></span>                    | <span data-ttu-id="99884-110">使用時機</span><span class="sxs-lookup"><span data-stu-id="99884-110">When to use</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99884-111">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="99884-111">**IDelaydC**</span></span>](idelaydc.md) | <span data-ttu-id="99884-112">使用來捕捉網路流量，並將它儲存在捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="99884-112">Use to capture network traffic and store it in a capture file.</span></span> <span data-ttu-id="99884-113">此介面是由網路監視器 UI 和其他 NPP 應用程式所使用，這些應用程式需要儲存已捕捉的網路資訊。</span><span class="sxs-lookup"><span data-stu-id="99884-113">This interface is used by the Network Monitor UI and other NPP applications, which require storing captured network information.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="99884-114">**IESP**</span><span class="sxs-lookup"><span data-stu-id="99884-114">**IESP**</span></span>](iesp.md)         | <span data-ttu-id="99884-115">用來以特殊的 ESP 檔案格式提供增強的統計資料。</span><span class="sxs-lookup"><span data-stu-id="99884-115">Used to provide enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="99884-116">NPP 應用程式會使用此介面，而這些應用程式需要 ESP 格式所提供的增強型統計資料。</span><span class="sxs-lookup"><span data-stu-id="99884-116">This interface is used by NPP applications that require the enhanced statistics provided by the ESP format.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="99884-117">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="99884-117">**IRTC**</span></span>](irtc.md)         | <span data-ttu-id="99884-118">用來捕捉即時網路流量，並在事件發生時觸發事件。</span><span class="sxs-lookup"><span data-stu-id="99884-118">Use to capture real-time network traffic and to trigger events when they occur.</span></span> <span data-ttu-id="99884-119">此介面是由需要執行時間捕捉的 NPP 應用程式所使用。</span><span class="sxs-lookup"><span data-stu-id="99884-119">This interface is used by NPP applications that require run-time captures.</span></span> <span data-ttu-id="99884-120">請注意，此介面不提供其他 NPP 介面所提供的統計資料，也不允許您將畫面格插入所捕捉的網路流量中。</span><span class="sxs-lookup"><span data-stu-id="99884-120">Note that this interface does not provide the statistics that the other NPP interfaces provide, nor does it allow you to insert frames into the captured network traffic.</span></span><br/> |
| [<span data-ttu-id="99884-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="99884-121">**IStats**</span></span>](istats.md)     | <span data-ttu-id="99884-122">使用以抓取捕捉統計資料，但不使用捕獲的框架。</span><span class="sxs-lookup"><span data-stu-id="99884-122">Use to retrieve capture statistics but not the captured frames.</span></span>                                                                                                                                                                                                                                                                                 |



 

 

 




