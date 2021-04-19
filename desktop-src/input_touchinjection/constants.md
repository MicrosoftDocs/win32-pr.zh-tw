---
title: 觸控式插入常數
description: 本節提供觸控式插入常數的參考規格。
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 76a763a7153bbb9aa67254ffeb5e994a55426e43
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106980254"
---
# <a name="touch-injection-constants"></a><span data-ttu-id="8872a-103">觸控式插入常數</span><span class="sxs-lookup"><span data-stu-id="8872a-103">Touch Injection constants</span></span>

<span data-ttu-id="8872a-104">本節提供 [觸控式插入](touch-injection-portal.md) 常數的參考規格。</span><span class="sxs-lookup"><span data-stu-id="8872a-104">This section provides the reference specifications for [Touch Injection](touch-injection-portal.md) constants.</span></span>

| <span data-ttu-id="8872a-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="8872a-105">Constant/value</span></span> | <span data-ttu-id="8872a-106">Description</span><span class="sxs-lookup"><span data-stu-id="8872a-106">Description</span></span> |
|---|---|
| <span data-ttu-id="8872a-107">**MAX_TOUCH_COUNT** 256</span><span class="sxs-lookup"><span data-stu-id="8872a-107">**MAX_TOUCH_COUNT** 256</span></span>                            | <span data-ttu-id="8872a-108">指定同時連絡人的最大數目。</span><span class="sxs-lookup"><span data-stu-id="8872a-108">Specifies the maximum number of simultaneous contacts.</span></span><br/> |
| <span data-ttu-id="8872a-109">**TOUCH_FEEDBACK_DEFAULT** 0x1</span><span class="sxs-lookup"><span data-stu-id="8872a-109">**TOUCH_FEEDBACK_DEFAULT** 0x1</span></span>    | <span data-ttu-id="8872a-110">指定預設觸控視覺效果。</span><span class="sxs-lookup"><span data-stu-id="8872a-110">Specifies default touch visualizations.</span></span><br/>                |
| <span data-ttu-id="8872a-111">**TOUCH_FEEDBACK_INDIRECT** 0x2</span><span class="sxs-lookup"><span data-stu-id="8872a-111">**TOUCH_FEEDBACK_INDIRECT** 0x2</span></span> | <span data-ttu-id="8872a-112">指定間接觸控視覺效果。</span><span class="sxs-lookup"><span data-stu-id="8872a-112">Specifies indirect touch visualizations.</span></span><br/>               |
| <span data-ttu-id="8872a-113">**TOUCH_FEEDBACK_NONE** 0x3</span><span class="sxs-lookup"><span data-stu-id="8872a-113">**TOUCH_FEEDBACK_NONE** 0x3</span></span>             | <span data-ttu-id="8872a-114">指定無觸控視覺效果。</span><span class="sxs-lookup"><span data-stu-id="8872a-114">Specifies no touch visualizations.</span></span><br/>                     |

## <a name="requirements"></a><span data-ttu-id="8872a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8872a-115">Requirements</span></span>

| <span data-ttu-id="8872a-116">需求</span><span class="sxs-lookup"><span data-stu-id="8872a-116">Requirement</span></span> | <span data-ttu-id="8872a-117">值</span><span class="sxs-lookup"><span data-stu-id="8872a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8872a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8872a-118">Minimum supported client</span></span> | <span data-ttu-id="8872a-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8872a-119">Windows 8 \[desktop apps only\]</span></span>                                           |
| <span data-ttu-id="8872a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8872a-120">Minimum supported server</span></span> | <span data-ttu-id="8872a-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8872a-121">Windows Server 2012 \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="8872a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8872a-122">Header</span></span>                   | <span data-ttu-id="8872a-123">Winuser。h</span><span class="sxs-lookup"><span data-stu-id="8872a-123">Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="8872a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8872a-124">See also</span></span>

[<span data-ttu-id="8872a-125">觸控式插入參考</span><span class="sxs-lookup"><span data-stu-id="8872a-125">Touch Injection Reference</span></span>](touch-injection-reference.md)
