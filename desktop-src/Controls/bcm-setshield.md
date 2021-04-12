---
title: 'BCM_SETSHIELD 訊息 (Commctrl .h) '
description: 設定指定之按鈕或命令連結的「提高許可權」狀態，以顯示提高許可權的圖示。 明確地傳送此訊息，或使用按鈕 \_ SetElevationRequiredState 宏。
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- BCM_SETSHIELD message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094439"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="24729-105">BCM \_ SETSHIELD 訊息</span><span class="sxs-lookup"><span data-stu-id="24729-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="24729-106">設定指定之按鈕或命令連結的「提高許可權」狀態，以顯示提高許可權的圖示。</span><span class="sxs-lookup"><span data-stu-id="24729-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="24729-107">明確地傳送此訊息，或使用 [**按鈕 \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) 宏。</span><span class="sxs-lookup"><span data-stu-id="24729-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24729-108">參數</span><span class="sxs-lookup"><span data-stu-id="24729-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24729-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24729-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24729-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="24729-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="24729-111">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24729-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24729-112">**布林** 值，為 **TRUE** 表示繪製提升許可權的圖示，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="24729-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24729-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="24729-113">Return value</span></span>

<span data-ttu-id="24729-114">如果成功，則傳回1，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24729-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="24729-115">備註</span><span class="sxs-lookup"><span data-stu-id="24729-115">Remarks</span></span>

<span data-ttu-id="24729-116">您必須將應用程式列入使用 comctl32.dll 第6版才能獲得這種功能。</span><span class="sxs-lookup"><span data-stu-id="24729-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="24729-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="24729-117">Requirements</span></span>



| <span data-ttu-id="24729-118">需求</span><span class="sxs-lookup"><span data-stu-id="24729-118">Requirement</span></span> | <span data-ttu-id="24729-119">值</span><span class="sxs-lookup"><span data-stu-id="24729-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24729-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24729-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24729-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24729-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24729-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24729-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24729-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24729-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24729-124">標頭</span><span class="sxs-lookup"><span data-stu-id="24729-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24729-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="24729-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





