---
description: WMI 高效能提供者會大幅增加 WMI 用戶端從 WMI 執行個體提供者取得資訊的速度。
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: 提升執行個體提供者的效率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850768"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a><span data-ttu-id="71500-103">提升執行個體提供者的效率</span><span class="sxs-lookup"><span data-stu-id="71500-103">Improving the Efficiency of an Instance Provider</span></span>

<span data-ttu-id="71500-104">WMI 高效能提供者會大幅增加 WMI 用戶端從 WMI 執行個體提供者取得資訊的速度。</span><span class="sxs-lookup"><span data-stu-id="71500-104">A WMI high-performance provider greatly increases the speed at which a WMI client can obtain information from a WMI instance provider.</span></span> <span data-ttu-id="71500-105">主要的變更是，高效能提供者會以同進程伺服器的形式執行至用戶端應用程式或 WMI。</span><span class="sxs-lookup"><span data-stu-id="71500-105">The main change is that a high-performance provider runs as an in-process server to either the client application or to WMI.</span></span> <span data-ttu-id="71500-106">藉由將提供者放在用戶端進程內，您可以加速兩者之間的互動。</span><span class="sxs-lookup"><span data-stu-id="71500-106">By placing the provider inside the client process, you can speed up the interaction between the two.</span></span>

<span data-ttu-id="71500-107">如需如何讓執行個體提供者成為高效能提供者的詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供](making-an-instance-provider-into-a-high-performance-provider.md)者。</span><span class="sxs-lookup"><span data-stu-id="71500-107">For more information about how to make your instance provider a high-performance provider, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

 

 



