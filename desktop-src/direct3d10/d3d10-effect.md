---
description: 這些常數是在建立效果來定義編譯行為或執行時間效果行為時使用。
ms.assetid: cff99200-8bdc-416c-b1a5-3ae515a17a17
title: D3D10_EFFECT 常數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c12b7a458bb7c97bb53436565513673006a2884
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317840"
---
# <a name="d3d10_effect-constants"></a><span data-ttu-id="2f15f-103">D3D10 \_ 效果常數</span><span class="sxs-lookup"><span data-stu-id="2f15f-103">D3D10\_EFFECT Constants</span></span>

<span data-ttu-id="2f15f-104">這些常數是在建立效果來定義編譯行為或執行時間效果行為時使用。</span><span class="sxs-lookup"><span data-stu-id="2f15f-104">These constants used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span>



| <span data-ttu-id="2f15f-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="2f15f-105">\#define</span></span>                                 | <span data-ttu-id="2f15f-106">值</span><span class="sxs-lookup"><span data-stu-id="2f15f-106">Value</span></span>        | <span data-ttu-id="2f15f-107">描述</span><span class="sxs-lookup"><span data-stu-id="2f15f-107">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f15f-108">D3D10 \_ 效果 \_ 編譯 \_ 子 \_ 效果</span><span class="sxs-lookup"><span data-stu-id="2f15f-108">D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT</span></span>    | <span data-ttu-id="2f15f-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="2f15f-109">1 << 0</span></span> | <span data-ttu-id="2f15f-110">將 fx 檔案編譯為子效果。</span><span class="sxs-lookup"><span data-stu-id="2f15f-110">Compile the .fx file to a child effect.</span></span> <span data-ttu-id="2f15f-111">子效果沒有任何共用值的初始化，因為這些值會在效果集區中初始化。</span><span class="sxs-lookup"><span data-stu-id="2f15f-111">Child effects have no initializes for any shared values because these are initialized in the effect pool.</span></span>                                                                                                           |
| <span data-ttu-id="2f15f-112">D3D10 \_ 效果 \_ 編譯 \_ 允許 \_ 緩慢的 \_ OPS</span><span class="sxs-lookup"><span data-stu-id="2f15f-112">D3D10\_EFFECT\_COMPILE\_ALLOW\_SLOW\_OPS</span></span> | <span data-ttu-id="2f15f-113">1 << 1</span><span class="sxs-lookup"><span data-stu-id="2f15f-113">1 << 1</span></span> | <span data-ttu-id="2f15f-114">預設會啟用效能模式。</span><span class="sxs-lookup"><span data-stu-id="2f15f-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="2f15f-115">效能模式防止非常值運算式出現在狀態物件定義中，因此不允許可變動狀態物件。</span><span class="sxs-lookup"><span data-stu-id="2f15f-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span> <span data-ttu-id="2f15f-116">指定此旗標將會停用模式，並允許可變狀態物件。</span><span class="sxs-lookup"><span data-stu-id="2f15f-116">Specifying this flag will disable the mode and allow for mutable state objects.</span></span> |
| <span data-ttu-id="2f15f-117">D3D10 \_ 效果 \_ 單個 \_ 執行緒</span><span class="sxs-lookup"><span data-stu-id="2f15f-117">D3D10\_EFFECT\_SINGLE\_THREADED</span></span>          | <span data-ttu-id="2f15f-118">1 << 3</span><span class="sxs-lookup"><span data-stu-id="2f15f-118">1 << 3</span></span> | <span data-ttu-id="2f15f-119">請勿嘗試與其他執行緒進行同步處理，將效果載入相同的集區。</span><span class="sxs-lookup"><span data-stu-id="2f15f-119">Do not attempt to synchronize with other threads loading effects into the same pool.</span></span>                                                                                                                                                                        |



 

<span data-ttu-id="2f15f-120">這些常數會定義為 d3d10effect 中的宏。</span><span class="sxs-lookup"><span data-stu-id="2f15f-120">These constants are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f15f-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f15f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f15f-122"> (Direct3D 10) 的效果常數 </span><span class="sxs-lookup"><span data-stu-id="2f15f-122">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



