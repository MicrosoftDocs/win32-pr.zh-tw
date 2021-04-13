---
title: 'CCM_SETWINDOWTHEME 訊息 (Commctrl .h) '
description: 設定控制項的視覺化樣式。
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- CCM_SETWINDOWTHEME message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465917"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="53896-104">CCM \_ SETWINDOWTHEME 訊息</span><span class="sxs-lookup"><span data-stu-id="53896-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="53896-105">設定控制項的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="53896-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53896-106">參數</span><span class="sxs-lookup"><span data-stu-id="53896-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53896-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53896-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="53896-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="53896-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="53896-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53896-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53896-110">包含要設定之控制項視覺化樣式的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="53896-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53896-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="53896-111">Return value</span></span>

<span data-ttu-id="53896-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="53896-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="53896-113">備註</span><span class="sxs-lookup"><span data-stu-id="53896-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53896-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="53896-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="53896-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="53896-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="53896-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="53896-116">Requirements</span></span>



| <span data-ttu-id="53896-117">需求</span><span class="sxs-lookup"><span data-stu-id="53896-117">Requirement</span></span> | <span data-ttu-id="53896-118">值</span><span class="sxs-lookup"><span data-stu-id="53896-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53896-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53896-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53896-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53896-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53896-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53896-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53896-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53896-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53896-123">標頭</span><span class="sxs-lookup"><span data-stu-id="53896-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53896-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="53896-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





