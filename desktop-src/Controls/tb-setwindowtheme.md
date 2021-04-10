---
title: 'TB_SETWINDOWTHEME 訊息 (Commctrl .h) '
description: 設定工具列控制項的視覺化樣式。
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- TB_SETWINDOWTHEME message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106583"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="8213b-104">TB \_ SETWINDOWTHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="8213b-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="8213b-105">設定工具列控制項的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="8213b-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8213b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8213b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8213b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8213b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8213b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8213b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8213b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8213b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8213b-110">Unicode 字串的指標，其中包含要設定的工具列視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="8213b-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8213b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8213b-111">Return value</span></span>

<span data-ttu-id="8213b-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="8213b-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8213b-113">備註</span><span class="sxs-lookup"><span data-stu-id="8213b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8213b-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="8213b-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8213b-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="8213b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="8213b-116">傳送此訊息相當於在工具列上呼叫 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) 和其工具提示控制項（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8213b-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="8213b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8213b-117">Requirements</span></span>



| <span data-ttu-id="8213b-118">需求</span><span class="sxs-lookup"><span data-stu-id="8213b-118">Requirement</span></span> | <span data-ttu-id="8213b-119">值</span><span class="sxs-lookup"><span data-stu-id="8213b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8213b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8213b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8213b-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8213b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8213b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8213b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8213b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8213b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8213b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8213b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8213b-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8213b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





