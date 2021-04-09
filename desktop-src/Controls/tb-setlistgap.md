---
title: 'TB_SETLISTGAP 訊息 (Commctrl .h) '
description: 設定特定工具列上工具列按鈕之間的距離。
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- TB_SETLISTGAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843052"
---
# <a name="tb_setlistgap-message"></a><span data-ttu-id="09d3f-104">TB \_ SETLISTGAP 訊息</span><span class="sxs-lookup"><span data-stu-id="09d3f-104">TB\_SETLISTGAP message</span></span>

<span data-ttu-id="09d3f-105">設定特定工具列上工具列按鈕之間的距離。</span><span class="sxs-lookup"><span data-stu-id="09d3f-105">Sets the distance between the toolbar buttons on a specific toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="09d3f-106">參數</span><span class="sxs-lookup"><span data-stu-id="09d3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d3f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09d3f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09d3f-108">工具列上按鈕之間的間距（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="09d3f-108">The gap, in pixels, between buttons on the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="09d3f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09d3f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09d3f-110">忽略。</span><span class="sxs-lookup"><span data-stu-id="09d3f-110">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d3f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="09d3f-111">Return value</span></span>

<span data-ttu-id="09d3f-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="09d3f-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09d3f-113">備註</span><span class="sxs-lookup"><span data-stu-id="09d3f-113">Remarks</span></span>

<span data-ttu-id="09d3f-114">按鈕之間的間距只適用于接收此訊息的工具列控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="09d3f-114">The gap between buttons only applies to the toolbar control window that receives this message.</span></span> <span data-ttu-id="09d3f-115">如果工具列目前是可見的，則接收此訊息會觸發工具列的重新繪製。</span><span class="sxs-lookup"><span data-stu-id="09d3f-115">Receipt of this message triggers a repaint of the toolbar, if the toolbar is currently visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d3f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="09d3f-116">Requirements</span></span>



| <span data-ttu-id="09d3f-117">需求</span><span class="sxs-lookup"><span data-stu-id="09d3f-117">Requirement</span></span> | <span data-ttu-id="09d3f-118">值</span><span class="sxs-lookup"><span data-stu-id="09d3f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09d3f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09d3f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09d3f-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d3f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09d3f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09d3f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09d3f-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d3f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09d3f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="09d3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d3f-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="09d3f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





