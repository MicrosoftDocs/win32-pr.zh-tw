---
description: 在您決定如何透過 CAPTUREFILTER 結構來組織篩選之後，必須配置並填入結構，然後透過設定 BLOB 將其傳遞至網路監視器驅動程式。
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: 執行捕獲篩選器程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853124"
---
# <a name="implementing-the-capture-filter-code"></a><span data-ttu-id="36b7f-103">執行捕獲篩選器程式碼</span><span class="sxs-lookup"><span data-stu-id="36b7f-103">Implementing the Capture Filter Code</span></span>

<span data-ttu-id="36b7f-104">在您決定如何透過 [**CAPTUREFILTER**](capturefilter.md) 結構來組織篩選之後，必須配置並填入結構，然後透過設定 BLOB 將其傳遞至網路監視器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="36b7f-104">After you determine how to organize your filter through a [**CAPTUREFILTER**](capturefilter.md) structure, you must allocate and fill in the structure, which is then passed to the Network Monitor driver through a configuration BLOB.</span></span>

<span data-ttu-id="36b7f-105">Direct NPP users 會將 capture 篩選器新增至傳遞給 **Connect**、Configure 或 both 的 [**設定**](configure.md)BLOB。</span><span class="sxs-lookup"><span data-stu-id="36b7f-105">Direct NPP users add the capture filter to the configuration BLOB that is passed to **Connect**, [**Configure**](configure.md), or both.</span></span> <span data-ttu-id="36b7f-106">如需可用來與 NPP 通訊的 COM 介面清單，請參閱 [NPP 介面](npp-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="36b7f-106">For a list of COM interfaces that you can use to communicate with the NPP, see [NPP Interfaces](npp-interfaces.md).</span></span>

 

 



