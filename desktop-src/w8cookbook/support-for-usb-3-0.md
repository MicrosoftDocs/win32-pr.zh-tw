---
title: USB 3.0 的支援
description: USB 3.0 的支援
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683222"
---
# <a name="support-for-usb-30"></a><span data-ttu-id="4106a-103">USB 3.0 的支援</span><span class="sxs-lookup"><span data-stu-id="4106a-103">Support for USB 3.0</span></span>

## <a name="platforms"></a><span data-ttu-id="4106a-104">平台</span><span class="sxs-lookup"><span data-stu-id="4106a-104">Platforms</span></span>

<span data-ttu-id="4106a-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="4106a-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="4106a-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4106a-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="4106a-107">Description</span><span class="sxs-lookup"><span data-stu-id="4106a-107">Description</span></span>

<span data-ttu-id="4106a-108">在 Windows 8 和 Windows Server 2012 中，我們新增了 USB 3.0 的支援。</span><span class="sxs-lookup"><span data-stu-id="4106a-108">In Windows 8 and Windows Server 2012, we added support for USB 3.0.</span></span> <span data-ttu-id="4106a-109">做法是新增軟體堆疊，以增強 USB 3.0 主機控制器的電源，稱為可延伸的主機控制器 (XHC) 。</span><span class="sxs-lookup"><span data-stu-id="4106a-109">We did this by adding a new software stack to power the USB 3.0 host controller, called an eXtensible Host Controller (XHC).</span></span> <span data-ttu-id="4106a-110">我們維護了介面同位、IRQL 層級、呼叫端內容、錯誤狀態、重試頻率等等。</span><span class="sxs-lookup"><span data-stu-id="4106a-110">We maintained interface parity, IRQL level, caller context, error status, retry frequency, and so on.</span></span> <span data-ttu-id="4106a-111">當您與透過 USB 2.0 或 USB 3.0 連接的裝置進行互動時，不會有任何差異。</span><span class="sxs-lookup"><span data-stu-id="4106a-111">There should be no difference for you when interacting with a device connected over USB 2.0 versus USB 3.0.</span></span>

<span data-ttu-id="4106a-112">但是，如果您要為新的 USB 3.0 裝置撰寫驅動程式，絕對可以選擇新的 USB 3.0 功能。</span><span class="sxs-lookup"><span data-stu-id="4106a-112">However, if you are writing a driver for a new, USB 3.0 device, definitely opt for new USB 3.0 capabilities.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4106a-113">表現</span><span class="sxs-lookup"><span data-stu-id="4106a-113">Manifestation</span></span>

<span data-ttu-id="4106a-114">整體 USB 裝置從電腦取用裝置傳輸的速度較快，且耗電量較低。</span><span class="sxs-lookup"><span data-stu-id="4106a-114">Device transfers are faster and less power is consumed from a PC by USB devices overall.</span></span> <span data-ttu-id="4106a-115">連線到 USB 3.0 埠時，現有的 USB 裝置可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4106a-115">There is a risk that existing USB devices may not function correctly when connected to a USB 3.0 port.</span></span> <span data-ttu-id="4106a-116">這應該不會發生，而且不是預期的，但因為支援 USB 3.0 的軟體是新的，所以這是一項風險。</span><span class="sxs-lookup"><span data-stu-id="4106a-116">This should not happen, and is not expected, but, because the software that powers USB 3.0 is new, it is a risk.</span></span>

 

 




