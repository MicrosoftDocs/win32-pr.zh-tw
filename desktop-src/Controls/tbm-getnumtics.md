---
title: 'TBM_GETNUMTICS 訊息 (Commctrl .h) '
description: 抓取在一個標記中的刻度數目。
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934089"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="2f39a-104">TBM \_ GETNUMTICS 訊息</span><span class="sxs-lookup"><span data-stu-id="2f39a-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="2f39a-105">抓取在一個標記中的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="2f39a-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f39a-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f39a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f39a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f39a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f39a-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2f39a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f39a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f39a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f39a-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2f39a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f39a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f39a-111">Return value</span></span>

<span data-ttu-id="2f39a-112">如果未設定 [滴答旗](trackbar-control-styles.md) 標，則會傳回2作為開始和結束刻度。</span><span class="sxs-lookup"><span data-stu-id="2f39a-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="2f39a-113">如果已設定 [**TBS \_ NOTICKS**](trackbar-control-styles.md) ，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="2f39a-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="2f39a-114">否則，它會採用範圍最小值和最大值之間的差異、除以滴答頻率，然後加上2。</span><span class="sxs-lookup"><span data-stu-id="2f39a-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f39a-115">備註</span><span class="sxs-lookup"><span data-stu-id="2f39a-115">Remarks</span></span>

<span data-ttu-id="2f39a-116">**TBM \_ GETNUMTICS** 訊息會計算所有的刻度，包括由顯示項所建立的第一個和最後一個刻度標記。</span><span class="sxs-lookup"><span data-stu-id="2f39a-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f39a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f39a-117">Requirements</span></span>



| <span data-ttu-id="2f39a-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f39a-118">Requirement</span></span> | <span data-ttu-id="2f39a-119">值</span><span class="sxs-lookup"><span data-stu-id="2f39a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f39a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f39a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f39a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f39a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f39a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f39a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f39a-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f39a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f39a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2f39a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f39a-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f39a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





