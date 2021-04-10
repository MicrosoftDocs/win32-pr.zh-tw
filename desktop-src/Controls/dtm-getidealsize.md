---
title: 'DTM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得在不剪切的情況下顯示控制項所需的大小。 請明確地傳送此訊息，或使用 DateTime \_ GetIdealSize 宏。
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187277"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="a1060-105">DTM \_ GETIDEALSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="a1060-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="a1060-106">取得在不剪切的情況下顯示控制項所需的大小。</span><span class="sxs-lookup"><span data-stu-id="a1060-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="a1060-107">請明確地傳送此訊息，或使用 [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) 宏。</span><span class="sxs-lookup"><span data-stu-id="a1060-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1060-108">參數</span><span class="sxs-lookup"><span data-stu-id="a1060-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1060-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1060-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1060-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="a1060-110">Not used.</span></span> <span data-ttu-id="a1060-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a1060-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a1060-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1060-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1060-113">要接收理想大小的 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="a1060-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="a1060-114">呼叫應用程式負責配置此結構。</span><span class="sxs-lookup"><span data-stu-id="a1060-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1060-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1060-115">Return value</span></span>

<span data-ttu-id="a1060-116">傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a1060-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1060-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1060-117">Requirements</span></span>



| <span data-ttu-id="a1060-118">需求</span><span class="sxs-lookup"><span data-stu-id="a1060-118">Requirement</span></span> | <span data-ttu-id="a1060-119">值</span><span class="sxs-lookup"><span data-stu-id="a1060-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1060-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1060-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1060-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1060-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1060-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1060-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1060-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1060-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1060-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a1060-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1060-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1060-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

