---
description: 如果預設選項的規則不符合應用程式的需求，則應用程式可以選擇以手動方式選取終端機。
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: 手動選取終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95335402690c57cc3f564f5d238ca031df4b3549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692235"
---
# <a name="manual-terminal-selection"></a><span data-ttu-id="905e5-103">手動選取終端機</span><span class="sxs-lookup"><span data-stu-id="905e5-103">Manual Terminal Selection</span></span>

<span data-ttu-id="905e5-104">如果預設選取範圍的規則不符合應用程式的需求，則應用程式可以選擇一律具有的終端機：也就是說，它可以使用 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) 來列舉呼叫上的資料流程，並選取適當資料流程上的終端機 (或者，如果是 multitrack 終端機，請建立資料流程的追蹤，然後選取資料流程) 上建立的追蹤。</span><span class="sxs-lookup"><span data-stu-id="905e5-104">If the rules of Default selection do not meet the needs of the application, the application has the option of selecting the terminal as it always has: that is, it can use [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) to enumerate the streams present on the call and select the terminal on the appropriate streams (or, in case of multitrack terminals, create tracks for the streams and select created tracks on the streams).</span></span>

 

 
