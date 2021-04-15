---
title: 計算的字元陣列
description: '\ Size \_ 為 \ 屬性工作表示陣列的上限，而 \ 的長度 \_ 為 \ 屬性工作表示要傳送的陣列元素數目。'
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463409"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="40133-103">計算的字元陣列</span><span class="sxs-lookup"><span data-stu-id="40133-103">Counted Character Arrays</span></span>

<span data-ttu-id="40133-104">\[ [Size \_ 為](/windows/desktop/Midl/size-is) \] attribute 指出陣列的上限，而 \[ [length \_ 為](/windows/desktop/Midl/length-is) \] attribute 表示要傳送的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="40133-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="40133-105">除了陣列之外，遠端程式原型還必須包含任何代表長度或大小的變數，這些變數會決定已傳送的陣列元素 (它們可以是不同的參數，或與結構中的字串一起組合) 。</span><span class="sxs-lookup"><span data-stu-id="40133-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="40133-106">這些屬性可以與寬字元或單一位元組字元陣列搭配使用，就如同使用其他類型的陣列一樣。</span><span class="sxs-lookup"><span data-stu-id="40133-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="40133-107">本節中的資訊說明字元陣列的遠端過程參數原型。</span><span class="sxs-lookup"><span data-stu-id="40133-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="40133-108">它分成下列主題：</span><span class="sxs-lookup"><span data-stu-id="40133-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="40133-109">[\[in、out、size \_ 為 \] 原型](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="40133-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="40133-110">[\[在中，大小 \_ 為和輸出，大小 \_ 為 \] 原型](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="40133-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 