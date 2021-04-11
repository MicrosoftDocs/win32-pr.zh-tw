---
description: TSPI 中使用不透明的控制碼來參考代表線條、電話和呼叫外觀的資料結構。
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: 不透明的控制碼和私用資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943599"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="c2463-103">不透明的控制碼和私用資料結構</span><span class="sxs-lookup"><span data-stu-id="c2463-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="c2463-104">TSPI 中使用不透明的控制碼來參考代表線條、電話和呼叫外觀的資料結構。</span><span class="sxs-lookup"><span data-stu-id="c2463-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="c2463-105">這些會顯示為大部分函式和回呼的參數。</span><span class="sxs-lookup"><span data-stu-id="c2463-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="c2463-106">有幾個函式是使用裝置識別碼來參考裝置，而不是不透明的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c2463-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="c2463-107">在這種情況下，參考會指向裝置本身，而不是資料結構。</span><span class="sxs-lookup"><span data-stu-id="c2463-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="c2463-108">以這種方式運作的函式通常是在建立資料結構和交換不透明的控制碼之前，于早期初始化時間呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="c2463-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="c2463-109">服務提供者必須決定如何解讀這些控制碼。</span><span class="sxs-lookup"><span data-stu-id="c2463-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="c2463-110">服務提供者通常會使用其資料結構的指標，或使用資料結構陣列中的索引做為不透明的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c2463-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="c2463-111">唯一的限制是服務提供者不能使用值0做為 [HDRVLINE](hdrvline.md)、HDRVCALL 或 [HDRVPHONE](hdrvphone.md)。</span><span class="sxs-lookup"><span data-stu-id="c2463-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="c2463-112">控制碼的值0或 **Null** 在某些作業中具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="c2463-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 



