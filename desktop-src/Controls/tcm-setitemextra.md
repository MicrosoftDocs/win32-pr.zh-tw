---
title: 'TCM_SETITEMEXTRA 訊息 (Commctrl .h) '
description: 設定在索引標籤控制項中，為應用程式定義資料保留的每個索引標籤的位元組數目。 您可以使用 TabCtrl SetItemExtra 宏明確地傳送此訊息 \_ 。
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093804"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="0ca4f-105">TCM \_ SETITEMEXTRA 訊息</span><span class="sxs-lookup"><span data-stu-id="0ca4f-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="0ca4f-106">設定在索引標籤控制項中，為應用程式定義資料保留的每個索引標籤的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="0ca4f-107">您可以使用 [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ca4f-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ca4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ca4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca4f-110">額外的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0ca4f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ca4f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0ca4f-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ca4f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ca4f-113">Return value</span></span>

<span data-ttu-id="0ca4f-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca4f-115">備註</span><span class="sxs-lookup"><span data-stu-id="0ca4f-115">Remarks</span></span>

<span data-ttu-id="0ca4f-116">根據預設，額外的位元組數目為四。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="0ca4f-117">變更額外位元組數目的應用程式無法使用 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構來取得和設定索引標籤的應用程式定義資料。相反地，您必須定義由 [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) 結構組成的新結構，後面接著應用程式定義的成員。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="0ca4f-118">應用程式應該只在索引標籤控制項未包含任何索引標籤時，變更額外的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="0ca4f-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca4f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ca4f-119">Requirements</span></span>



| <span data-ttu-id="0ca4f-120">需求</span><span class="sxs-lookup"><span data-stu-id="0ca4f-120">Requirement</span></span> | <span data-ttu-id="0ca4f-121">值</span><span class="sxs-lookup"><span data-stu-id="0ca4f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca4f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ca4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ca4f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ca4f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ca4f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ca4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ca4f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ca4f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ca4f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0ca4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ca4f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ca4f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





