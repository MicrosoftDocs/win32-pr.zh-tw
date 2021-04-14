---
title: 'TTM_SETWINDOWTHEME 訊息 (Commctrl .h) '
description: 設定工具提示控制項的視覺化樣式。
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- TTM_SETWINDOWTHEME message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c3f25b62bf0fe38a679234183cd5046f60784f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509299"
---
# <a name="ttm_setwindowtheme-message"></a><span data-ttu-id="efb62-104">TTM \_ SETWINDOWTHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="efb62-104">TTM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="efb62-105">設定工具提示控制項的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="efb62-105">Sets the visual style of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="efb62-106">參數</span><span class="sxs-lookup"><span data-stu-id="efb62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb62-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efb62-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="efb62-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="efb62-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="efb62-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efb62-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efb62-110">包含要設定之工具提示視覺化樣式的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="efb62-110">Pointer to a Unicode string that contains the tooltip visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb62-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="efb62-111">Return value</span></span>

<span data-ttu-id="efb62-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="efb62-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb62-113">備註</span><span class="sxs-lookup"><span data-stu-id="efb62-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="efb62-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="efb62-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="efb62-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="efb62-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efb62-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="efb62-116">Requirements</span></span>



| <span data-ttu-id="efb62-117">需求</span><span class="sxs-lookup"><span data-stu-id="efb62-117">Requirement</span></span> | <span data-ttu-id="efb62-118">值</span><span class="sxs-lookup"><span data-stu-id="efb62-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efb62-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efb62-119">Minimum supported client</span></span><br/> | <span data-ttu-id="efb62-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efb62-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efb62-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efb62-121">Minimum supported server</span></span><br/> | <span data-ttu-id="efb62-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efb62-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efb62-123">標頭</span><span class="sxs-lookup"><span data-stu-id="efb62-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="efb62-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="efb62-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





