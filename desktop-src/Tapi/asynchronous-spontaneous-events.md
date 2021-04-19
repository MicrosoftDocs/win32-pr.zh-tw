---
description: 除了上述的非同步事件之外，還有另一個類別。
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: 非同步自發事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975174"
---
# <a name="asynchronous-spontaneous-events"></a><span data-ttu-id="db232-103">非同步自發事件</span><span class="sxs-lookup"><span data-stu-id="db232-103">Asynchronous Spontaneous Events</span></span>

<span data-ttu-id="db232-104">除了上述的非同步事件之外，還有另一個類別。</span><span class="sxs-lookup"><span data-stu-id="db232-104">There is another class of asynchronous events besides those described above.</span></span> <span data-ttu-id="db232-105">這些事件是「自發」的意義，因為它們不是對應要求的直接結果。</span><span class="sxs-lookup"><span data-stu-id="db232-105">These events are "spontaneous" in the sense that they are not direct results of corresponding requests.</span></span> <span data-ttu-id="db232-106">在這種情況下，偵測到傳入的呼叫抵達時，或從「響鈴」進入「正在接聽」狀態時，就會偵測到這些事件。</span><span class="sxs-lookup"><span data-stu-id="db232-106">These events are detected in such cases as when an incoming call arrives, or when an outbound call goes from a "ringing" to an "answering" state.</span></span> <span data-ttu-id="db232-107">當 TAPI 首次初始化與特定裝置的 TSPI 互動時，它會傳遞回呼程式的指標，以針對報告這類自發事件進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="db232-107">When TAPI first initializes interactions with the TSPI for a particular device, it passes a pointer to a callback procedure to be called for reporting such spontaneous events.</span></span> <span data-ttu-id="db232-108">除了這個程式指標，也是服務提供者以其中一個實際參數的形式包含在回呼中的裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="db232-108">Along with this procedure pointer is a device handle that the service provider includes as one of the actual parameters to the callback.</span></span>

 

 



