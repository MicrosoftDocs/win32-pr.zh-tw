---
title: 'DTM_SETMCFONT 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的子月曆控制項所使用的字型。 您可以明確地傳送此訊息，或使用 DateTime \_ SetMonthCalFont 宏。
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466117"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="56348-105">DTM \_ SETMCFONT 訊息</span><span class="sxs-lookup"><span data-stu-id="56348-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="56348-106">設定日期和時間選擇器 (DTP) 控制項的子月曆控制項所使用的字型。</span><span class="sxs-lookup"><span data-stu-id="56348-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="56348-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) 宏。</span><span class="sxs-lookup"><span data-stu-id="56348-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="56348-108">參數</span><span class="sxs-lookup"><span data-stu-id="56348-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56348-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56348-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56348-110">將設定之字型的控制碼。</span><span class="sxs-lookup"><span data-stu-id="56348-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="56348-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56348-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56348-112">指定是否應該在設定字型時立即重新繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="56348-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="56348-113">將此參數設定為 **TRUE** 會使控制項重新繪製。</span><span class="sxs-lookup"><span data-stu-id="56348-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56348-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="56348-114">Return value</span></span>

<span data-ttu-id="56348-115">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="56348-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="56348-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="56348-116">Requirements</span></span>



| <span data-ttu-id="56348-117">需求</span><span class="sxs-lookup"><span data-stu-id="56348-117">Requirement</span></span> | <span data-ttu-id="56348-118">值</span><span class="sxs-lookup"><span data-stu-id="56348-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56348-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56348-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56348-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56348-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56348-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56348-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56348-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56348-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56348-123">標頭</span><span class="sxs-lookup"><span data-stu-id="56348-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56348-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="56348-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





