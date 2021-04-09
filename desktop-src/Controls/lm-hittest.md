---
title: 'LM_HITTEST 訊息 (Commctrl .h) '
description: 判斷使用者是否按一下指定的連結。
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843100"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="6a1b1-104">LM \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="6a1b1-104">LM\_HITTEST message</span></span>

<span data-ttu-id="6a1b1-105">判斷使用者是否按一下指定的連結。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a1b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a1b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a1b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a1b1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6a1b1-108">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="6a1b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a1b1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6a1b1-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a>結構的指標，要填入使用者所按下的連結相關資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a1b1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a1b1-111">Return value</span></span>

<span data-ttu-id="6a1b1-112">如果使用者按一下連結， **則傳回 TRUE** ，否則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1b1-113">備註</span><span class="sxs-lookup"><span data-stu-id="6a1b1-113">Remarks</span></span>

<span data-ttu-id="6a1b1-114">如果 **LM \_ system.windows.media.visualtreehelper.hittest** 訊息成功，系統會填入 [**LITEM. Ashraf**](/windows/win32/api/commctrl/ns-commctrl-litem) 和 **LITEM. szID**。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="6a1b1-115">如果 **LM \_ system.windows.media.visualtreehelper.hittest** 訊息失敗，請勿假設 **LITEM** 中的任何資訊都有效。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="6a1b1-116">若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6a1b1-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6a1b1-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a1b1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a1b1-118">Requirements</span></span>



| <span data-ttu-id="6a1b1-119">需求</span><span class="sxs-lookup"><span data-stu-id="6a1b1-119">Requirement</span></span> | <span data-ttu-id="6a1b1-120">值</span><span class="sxs-lookup"><span data-stu-id="6a1b1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1b1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a1b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a1b1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a1b1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a1b1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a1b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a1b1-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a1b1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a1b1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6a1b1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a1b1-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a1b1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





