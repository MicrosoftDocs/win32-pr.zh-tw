---
title: 觸控點擊測試分數
description: 下列常數會識別物件的可能點擊測試分數（相對於與 touch contact 區域交集的其他物件）。
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508468"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="038b1-103">觸控點擊測試分數</span><span class="sxs-lookup"><span data-stu-id="038b1-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="038b1-104">下列常數會識別物件的可能點擊測試分數（相對於與 touch contact 區域交集的其他物件）。</span><span class="sxs-lookup"><span data-stu-id="038b1-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="038b1-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="038b1-105">Constant/value</span></span> | <span data-ttu-id="038b1-106">Description</span><span class="sxs-lookup"><span data-stu-id="038b1-106">Description</span></span> |
|---|---|
| <span data-ttu-id="038b1-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span><span class="sxs-lookup"><span data-stu-id="038b1-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="038b1-108">物件是最可能的目標。</span><span class="sxs-lookup"><span data-stu-id="038b1-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="038b1-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span><span class="sxs-lookup"><span data-stu-id="038b1-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="038b1-110">物件是最不可能的目標。</span><span class="sxs-lookup"><span data-stu-id="038b1-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="038b1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="038b1-111">Requirements</span></span>

| <span data-ttu-id="038b1-112">需求</span><span class="sxs-lookup"><span data-stu-id="038b1-112">Requirement</span></span> | <span data-ttu-id="038b1-113">值</span><span class="sxs-lookup"><span data-stu-id="038b1-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="038b1-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="038b1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="038b1-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="038b1-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="038b1-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="038b1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="038b1-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="038b1-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="038b1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="038b1-118">Header</span></span><br/>                   | <span data-ttu-id="038b1-119">Winuser。h</span><span class="sxs-lookup"><span data-stu-id="038b1-119">Winuser.h</span></span> |
