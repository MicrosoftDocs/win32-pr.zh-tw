---
description: TSPI 所定義的一些類型是不透明的控制碼。
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: 不透明控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512060"
---
# <a name="opaque-handles"></a><span data-ttu-id="b25a1-103">不透明控制碼</span><span class="sxs-lookup"><span data-stu-id="b25a1-103">Opaque Handles</span></span>

<span data-ttu-id="b25a1-104">TSPI 所定義的一些類型是不透明的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b25a1-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="b25a1-105">這些會在 TSPI 中用來做為私用資料結構的公用參考。</span><span class="sxs-lookup"><span data-stu-id="b25a1-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="b25a1-106">這可讓您針對介面程式提供的參數進行類型檢查，同時仍然提供類型保護的量值。</span><span class="sxs-lookup"><span data-stu-id="b25a1-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="b25a1-107">只有私用資料結構的擁有者知道如何將不透明的型別解讀為其資料結構標記法的參考。</span><span class="sxs-lookup"><span data-stu-id="b25a1-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="b25a1-108">如需如何使用不透明控制碼的範例，請考慮使用電話裝置。</span><span class="sxs-lookup"><span data-stu-id="b25a1-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="b25a1-109">TAPI 和服務提供者通常會維護代表其個別裝置觀點的資料結構。</span><span class="sxs-lookup"><span data-stu-id="b25a1-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="b25a1-110">在 TAPI 和服務提供者所維護的一般電話資料結構中，每個都包含其他資料結構的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="b25a1-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="b25a1-111">這些都是在早期的初始化步驟中進行交換。</span><span class="sxs-lookup"><span data-stu-id="b25a1-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="b25a1-112">當 TAPI 呼叫 TSPI 函式時，它會傳遞不透明的控制碼來參考裝置。</span><span class="sxs-lookup"><span data-stu-id="b25a1-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="b25a1-113">服務提供者知道如何將此解析為參考 (箭號) 至其資料結構。</span><span class="sxs-lookup"><span data-stu-id="b25a1-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="b25a1-114">當服務提供者在 TAPI 中呼叫回呼函式時，就會發生類似的進程。</span><span class="sxs-lookup"><span data-stu-id="b25a1-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



