---
title: '結構 (指標輸入訊息和通知) '
description: 本節中的主題提供指標輸入訊息和通知結構的參考規格。
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106996118"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="1d1af-103">指標輸入訊息和通知結構</span><span class="sxs-lookup"><span data-stu-id="1d1af-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="1d1af-104">本節中的主題提供 [指標輸入訊息和通知](messages-and-notifications-portal.md) 結構的參考規格。</span><span class="sxs-lookup"><span data-stu-id="1d1af-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1d1af-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="1d1af-105">In this section</span></span>



| <span data-ttu-id="1d1af-106">主題</span><span class="sxs-lookup"><span data-stu-id="1d1af-106">Topic</span></span>                                                                            | <span data-ttu-id="1d1af-107">描述</span><span class="sxs-lookup"><span data-stu-id="1d1af-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d1af-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="1d1af-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="1d1af-109">定義表示訊息取用者之轉換的矩陣。</span><span class="sxs-lookup"><span data-stu-id="1d1af-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="1d1af-110">您可以使用這個矩陣，將指標輸入資料從用戶端座標轉換成螢幕座標，而反向可用來將指標輸入資料從螢幕座標轉換成用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="1d1af-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="1d1af-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="1d1af-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="1d1af-112">包含所有指標類型通用的基本指標資訊。</span><span class="sxs-lookup"><span data-stu-id="1d1af-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="1d1af-113">應用程式可以使用 [**GetPointerInfo**](/previous-versions/windows/desktop/api)、 [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api)、 [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) 和 [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) 函數來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="1d1af-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="1d1af-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="1d1af-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="1d1af-115">定義所有指標類型通用的基本畫筆資訊。</span><span class="sxs-lookup"><span data-stu-id="1d1af-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="1d1af-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="1d1af-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="1d1af-117">定義所有指標類型通用的基本觸控資訊。</span><span class="sxs-lookup"><span data-stu-id="1d1af-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="1d1af-118">**TOUCHPREDICTIONPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="1d1af-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="1d1af-119">包含可用來預測觸控目標的硬體輸入詳細資料，並在處理包含距離和速度資料的觸控和手勢輸入時協助補償硬體延遲。</span><span class="sxs-lookup"><span data-stu-id="1d1af-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="1d1af-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d1af-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d1af-121">指標輸入訊息參考</span><span class="sxs-lookup"><span data-stu-id="1d1af-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





