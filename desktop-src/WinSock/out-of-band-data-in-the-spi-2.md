---
description: 支援資料流程樣式通訊端之頻外資料 (OOB) 抽象層的服務提供者必須遵守本節中的語法。
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: SPI 中的頻外資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026211"
---
# <a name="out-of-band-data-in-the-spi"></a><span data-ttu-id="a7ba1-103">SPI 中的頻外資料</span><span class="sxs-lookup"><span data-stu-id="a7ba1-103">Out-of-Band Data in the SPI</span></span>

<span data-ttu-id="a7ba1-104">支援資料流程樣式通訊端之頻外資料 (OOB) 抽象層的服務提供者必須遵守本節中的語法。</span><span class="sxs-lookup"><span data-stu-id="a7ba1-104">The service providers which support the out-of-band data (OOB) abstraction for the stream-style sockets must adhere to the semantics in this section.</span></span> <span data-ttu-id="a7ba1-105">我們將以與通訊協定無關的方式來描述 OOB 資料處理。</span><span class="sxs-lookup"><span data-stu-id="a7ba1-105">We will describe OOB data handling in a protocol-independent manner.</span></span> <span data-ttu-id="a7ba1-106">請參閱 [Winsock 附件](winsock-annexes.md) ，以取得使用 tcp/ip 服務提供者中的緊急資料所執行的 OOB 資料討論。</span><span class="sxs-lookup"><span data-stu-id="a7ba1-106">Please refer to the [Winsock Annexes](winsock-annexes.md) for a discussion of OOB data implemented using urgent data in TCP/IP service providers.</span></span> <span data-ttu-id="a7ba1-107">在下列情況下，使用 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 也會套用至 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a7ba1-107">In the following, the use of [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) also applies to [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span></span>

 

 
