---
title: 'CCM_SETVERSION 訊息 (Commctrl .h) '
description: 此訊息是用來通知控制項您預期會有與特定版本相關聯的行為。
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025258"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="7a5c3-104">CCM \_ SETVERSION 訊息</span><span class="sxs-lookup"><span data-stu-id="7a5c3-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="7a5c3-105">此訊息是用來通知控制項您預期會有與特定版本相關聯的行為。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a5c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a5c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a5c3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a5c3-108">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="7a5c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a5c3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7a5c3-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5c3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a5c3-111">Return value</span></span>

<span data-ttu-id="7a5c3-112">傳回先前 **CCM \_ SETVERSION** 訊息中指定的版本。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="7a5c3-113">如果 *wParam* 設定為大於目前 DLL 版本的值，則會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a5c3-114">備註</span><span class="sxs-lookup"><span data-stu-id="7a5c3-114">Remarks</span></span>

<span data-ttu-id="7a5c3-115">在少數情況下，控制項的行為可能會不同，視版本而定。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="7a5c3-116">這主要適用于在較新版本中修正的 bug。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="7a5c3-117">**CCM \_ SETVERSION** 訊息可讓您通知控制項預期的行為。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="7a5c3-118">您可以藉由傳送 [**CCM \_ GETVERSION**](ccm-getversion.md) 訊息來判斷所指定的版本。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="7a5c3-119">如需如何使用此訊息的範例，請參閱 [使用 List-View 和 Tree-View 控制項的自訂繪製](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="7a5c3-120">如果您已安裝 ComCtl32.dll 版本6，不論您在 *wParam* 中設定的值為何， **CCM \_ SETVERSION** 訊息都會傳回第6版。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="7a5c3-121">此訊息只會設定其傳送目標控制項的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7a5c3-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7a5c3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a5c3-122">Requirements</span></span>



| <span data-ttu-id="7a5c3-123">需求</span><span class="sxs-lookup"><span data-stu-id="7a5c3-123">Requirement</span></span> | <span data-ttu-id="7a5c3-124">值</span><span class="sxs-lookup"><span data-stu-id="7a5c3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5c3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a5c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5c3-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a5c3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a5c3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a5c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5c3-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a5c3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a5c3-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7a5c3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5c3-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a5c3-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





