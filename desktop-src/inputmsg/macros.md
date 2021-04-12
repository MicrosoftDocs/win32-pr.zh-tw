---
title: 巨集
description: 本節中的主題提供指標輸入訊息的參考規格，以及用來從指標輸入訊息參數取得資訊的通知宏。
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2020
ms.locfileid: "104374210"
---
# <a name="macros"></a><span data-ttu-id="b94b8-103">巨集</span><span class="sxs-lookup"><span data-stu-id="b94b8-103">Macros</span></span>

<span data-ttu-id="b94b8-104">本節中的主題提供 [指標輸入訊息](messages-and-notifications-portal.md) 的參考規格，以及用來從指標輸入訊息參數取得資訊的通知宏。</span><span class="sxs-lookup"><span data-stu-id="b94b8-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b94b8-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="b94b8-105">In this section</span></span>



| <span data-ttu-id="b94b8-106">主題</span><span class="sxs-lookup"><span data-stu-id="b94b8-106">Topic</span></span>                                                                                  | <span data-ttu-id="b94b8-107">描述</span><span class="sxs-lookup"><span data-stu-id="b94b8-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b94b8-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="b94b8-109">使用指定的值，抓取指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="b94b8-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="b94b8-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="b94b8-111">檢查指定的指標訊息是否視為刻意而非意外的。</span><span class="sxs-lookup"><span data-stu-id="b94b8-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="b94b8-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="b94b8-113">檢查指定的指標輸入是否突然結束，或是否無效，指出未完成互動。</span><span class="sxs-lookup"><span data-stu-id="b94b8-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="b94b8-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="b94b8-115">檢查指定的指標是否花費第五個動作。</span><span class="sxs-lookup"><span data-stu-id="b94b8-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="b94b8-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="b94b8-117">檢查指定的指標是否採取第一個動作。</span><span class="sxs-lookup"><span data-stu-id="b94b8-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="b94b8-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="b94b8-119">檢查指標宏是否設定指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="b94b8-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="b94b8-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="b94b8-121">檢查指定的指標是否採取第四個動作。</span><span class="sxs-lookup"><span data-stu-id="b94b8-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="b94b8-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="b94b8-123">檢查指定的指標是否為 contact。</span><span class="sxs-lookup"><span data-stu-id="b94b8-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="b94b8-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="b94b8-125">檢查指定的指標是否在範圍內。</span><span class="sxs-lookup"><span data-stu-id="b94b8-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="b94b8-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="b94b8-127">檢查指定的指標是否為新指標。</span><span class="sxs-lookup"><span data-stu-id="b94b8-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="b94b8-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="b94b8-129">檢查指定的指標是否為主要指標。</span><span class="sxs-lookup"><span data-stu-id="b94b8-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="b94b8-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="b94b8-131">檢查指定的指標是否採取第二個動作。</span><span class="sxs-lookup"><span data-stu-id="b94b8-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="b94b8-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="b94b8-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="b94b8-133">檢查指定的指標是否採取第三個動作。</span><span class="sxs-lookup"><span data-stu-id="b94b8-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="b94b8-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="b94b8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b94b8-135">指標輸入訊息參考</span><span class="sxs-lookup"><span data-stu-id="b94b8-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





