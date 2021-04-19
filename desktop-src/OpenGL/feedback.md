---
title: 意見反應
description: 在意見反應模式中，每個要進行柵格化的基本物件都會產生一個值區塊，而這些值會複製到意見陣列中。
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- 意見反應模式、OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106976637"
---
# <a name="feedback-mode"></a><span data-ttu-id="5833a-104">意見反應模式</span><span class="sxs-lookup"><span data-stu-id="5833a-104">Feedback mode</span></span>

<span data-ttu-id="5833a-105">在意見反應模式中，每個要進行柵格化的基本物件都會產生一個值區塊，而這些值會複製到意見陣列中。</span><span class="sxs-lookup"><span data-stu-id="5833a-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="5833a-106">提供此陣列的 [**glFeedbackBuffer**](glfeedbackbuffer.md)，您必須先呼叫此陣列，才能將 OpenGL 放入意見反應模式。</span><span class="sxs-lookup"><span data-stu-id="5833a-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="5833a-107">值的每個區塊都會以表示基本類型的程式碼開頭，後面接著描述基本頂點和相關資料的值。</span><span class="sxs-lookup"><span data-stu-id="5833a-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="5833a-108">此外，也會為點陣圖和圖元矩形寫入專案。</span><span class="sxs-lookup"><span data-stu-id="5833a-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="5833a-109">在您呼叫 [**glRenderMode**](glrendermode.md) 讓 OpenGL 離開意見反應模式之前，不保證會將值寫入意見陣列中。</span><span class="sxs-lookup"><span data-stu-id="5833a-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="5833a-110">您可以使用 [**glPassThrough**](glpassthrough.md) 來提供以意見反應模式傳回的標記，就像是基本的標記一樣。</span><span class="sxs-lookup"><span data-stu-id="5833a-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




