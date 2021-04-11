---
title: 'TDM_SET_MARQUEE_PROGRESS_BAR 訊息 (Commctrl .h) '
description: 指出工作對話方塊的裝載進度列是否應顯示在捲軸模式中。
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105971"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="f7127-104">TDM \_ SET \_ 天棚 \_ 進度列 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="f7127-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="f7127-105">指出工作對話方塊的裝載進度列是否應顯示在捲軸模式中。</span><span class="sxs-lookup"><span data-stu-id="f7127-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7127-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7127-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7127-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7127-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7127-108">**布林** 值，指出進度列是否應顯示在捲軸模式中。</span><span class="sxs-lookup"><span data-stu-id="f7127-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="f7127-109">值為 **TRUE** 會開啟字幕模式，而值為 **FALSE** 則會關閉字幕模式。</span><span class="sxs-lookup"><span data-stu-id="f7127-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="f7127-110">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7127-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7127-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f7127-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7127-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7127-112">Return value</span></span>

<span data-ttu-id="f7127-113">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f7127-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7127-114">備註</span><span class="sxs-lookup"><span data-stu-id="f7127-114">Remarks</span></span>

<span data-ttu-id="f7127-115">如需捲軸模式的詳細資訊，請參閱 [進度列控制項](progress-bar-control.md)。</span><span class="sxs-lookup"><span data-stu-id="f7127-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7127-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7127-116">Requirements</span></span>



| <span data-ttu-id="f7127-117">需求</span><span class="sxs-lookup"><span data-stu-id="f7127-117">Requirement</span></span> | <span data-ttu-id="f7127-118">值</span><span class="sxs-lookup"><span data-stu-id="f7127-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7127-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7127-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7127-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7127-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7127-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7127-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7127-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7127-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7127-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f7127-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7127-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7127-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





