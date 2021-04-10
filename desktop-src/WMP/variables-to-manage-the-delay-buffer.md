---
title: 管理延遲緩衝區的變數
description: 管理延遲緩衝區的變數
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Windows Media Player 外掛程式，Echo 範例串流資源
- 外掛程式，Echo 範例串流資源
- 數位信號處理外掛程式，Echo 範例串流資源
- DSP 外掛程式，Echo 範例串流資源
- Echo DSP 外掛程式範例，串流資源
- Echo DSP 外掛程式範例，延遲緩衝區
- 延遲緩衝區
- 緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183671"
---
# <a name="variables-to-manage-the-delay-buffer"></a><span data-ttu-id="06fa4-111">管理延遲緩衝區的變數</span><span class="sxs-lookup"><span data-stu-id="06fa4-111">Variables to Manage the Delay Buffer</span></span>

<span data-ttu-id="06fa4-112">您必須加入管理延遲緩衝區所需的成員變數宣告。</span><span class="sxs-lookup"><span data-stu-id="06fa4-112">You must add the declarations for the member variables you need to manage the delay buffer.</span></span> <span data-ttu-id="06fa4-113">在「私用」區段中，將下列宣告新增至 Echo：</span><span class="sxs-lookup"><span data-stu-id="06fa4-113">Add the following declarations to Echo.h in the "private" section:</span></span>


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



<span data-ttu-id="06fa4-114">將下列程式碼新增至 CEcho 的函式，以初始化延遲緩衝區變數：</span><span class="sxs-lookup"><span data-stu-id="06fa4-114">Add the following code to the CEcho constructor to initialize the delay buffer variables:</span></span>


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a><span data-ttu-id="06fa4-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="06fa4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06fa4-116">**使用串流資源**</span><span class="sxs-lookup"><span data-stu-id="06fa4-116">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




