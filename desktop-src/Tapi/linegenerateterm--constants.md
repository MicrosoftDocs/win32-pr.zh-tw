---
description: LINEGENERATETERM \_ 位旗標常數描述結束數位或音訊產生的條件。
ms.assetid: 5cdc43c0-2349-4ffc-9bf7-3b498b35db95
title: 'LINEGENERATETERM_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6804b09879471a77780a95ca4ed35b7aaa5b6e1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991036"
---
# <a name="linegenerateterm_-constants"></a><span data-ttu-id="f3de8-103">LINEGENERATETERM \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f3de8-103">LINEGENERATETERM\_ Constants</span></span>

<span data-ttu-id="f3de8-104">**LINEGENERATETERM \_** 位旗標常數描述結束數位或音訊產生的條件。</span><span class="sxs-lookup"><span data-stu-id="f3de8-104">The **LINEGENERATETERM\_** bit-flag constants describe the conditions under which digit or tone generation is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="f3de8-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="f3de8-105"><span id="LINEGENERATETERM_CANCEL"></span><span id="linegenerateterm_cancel"></span>**LINEGENERATETERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3de8-106">此應用程式、另一個應用程式已取消數位或語氣產生要求，或因為呼叫終止。</span><span class="sxs-lookup"><span data-stu-id="f3de8-106">The digit or tone generation request was canceled by this application, by another application, or because the call terminated.</span></span> <span data-ttu-id="f3de8-107">當數位或語氣產生因為服務提供者的內部失敗而無法完成時，也會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="f3de8-107">This value can also be returned when digit or tone generation cannot be completed due to internal failure of the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3de8-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="f3de8-108"><span id="LINEGENERATETERM_DONE"></span><span id="linegenerateterm_done"></span>**LINEGENERATETERM\_DONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3de8-109">要求的持續時間已產生要求的位數或要求的色調。</span><span class="sxs-lookup"><span data-stu-id="f3de8-109">The requested number of digits or requested tones have been generated for the requested duration.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3de8-110">備註</span><span class="sxs-lookup"><span data-stu-id="f3de8-110">Remarks</span></span>

<span data-ttu-id="f3de8-111">無延伸。</span><span class="sxs-lookup"><span data-stu-id="f3de8-111">No extensibility.</span></span> <span data-ttu-id="f3de8-112">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="f3de8-112">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3de8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3de8-113">Requirements</span></span>



| <span data-ttu-id="f3de8-114">需求</span><span class="sxs-lookup"><span data-stu-id="f3de8-114">Requirement</span></span> | <span data-ttu-id="f3de8-115">值</span><span class="sxs-lookup"><span data-stu-id="f3de8-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f3de8-116">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f3de8-116">TAPI version</span></span><br/> | <span data-ttu-id="f3de8-117">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f3de8-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f3de8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f3de8-118">Header</span></span><br/>       | <dl> <span data-ttu-id="f3de8-119"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="f3de8-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




