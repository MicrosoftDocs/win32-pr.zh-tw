---
title: 'RB_SETWINDOWTHEME 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的視覺化樣式。
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- RB_SETWINDOWTHEME message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104778"
---
# <a name="rb_setwindowtheme-message"></a><span data-ttu-id="b0e1c-104">RB \_ SETWINDOWTHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="b0e1c-104">RB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="b0e1c-105">設定 Rebar 控制項的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="b0e1c-105">Sets the visual style of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0e1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e1c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0e1c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b0e1c-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b0e1c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b0e1c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0e1c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e1c-110">Unicode 字串的指標，其中包含要設定的 Rebar 視覺效果樣式。</span><span class="sxs-lookup"><span data-stu-id="b0e1c-110">Pointer to a Unicode string that contains the rebar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e1c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0e1c-111">Return value</span></span>

<span data-ttu-id="b0e1c-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="b0e1c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e1c-113">備註</span><span class="sxs-lookup"><span data-stu-id="b0e1c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0e1c-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="b0e1c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b0e1c-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="b0e1c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0e1c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0e1c-116">Requirements</span></span>



| <span data-ttu-id="b0e1c-117">需求</span><span class="sxs-lookup"><span data-stu-id="b0e1c-117">Requirement</span></span> | <span data-ttu-id="b0e1c-118">值</span><span class="sxs-lookup"><span data-stu-id="b0e1c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e1c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0e1c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e1c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0e1c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0e1c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0e1c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e1c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0e1c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0e1c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b0e1c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e1c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e1c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





