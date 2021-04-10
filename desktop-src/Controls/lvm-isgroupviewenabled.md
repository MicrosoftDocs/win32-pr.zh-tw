---
title: 'LVM_ISGROUPVIEWENABLED 訊息 (Commctrl .h) '
description: 檢查清單視圖控制項是否已啟用群組視圖。
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- LVM_ISGROUPVIEWENABLED message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934888"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="6f364-104">LVM \_ ISGROUPVIEWENABLED 訊息</span><span class="sxs-lookup"><span data-stu-id="6f364-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="6f364-105">檢查清單視圖控制項是否已啟用群組視圖。</span><span class="sxs-lookup"><span data-stu-id="6f364-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f364-106">參數</span><span class="sxs-lookup"><span data-stu-id="6f364-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f364-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f364-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f364-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6f364-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f364-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f364-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6f364-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6f364-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f364-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f364-111">Return value</span></span>

<span data-ttu-id="6f364-112">如果已啟用群組視圖，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6f364-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f364-113">備註</span><span class="sxs-lookup"><span data-stu-id="6f364-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f364-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="6f364-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6f364-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6f364-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f364-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f364-116">Requirements</span></span>



| <span data-ttu-id="6f364-117">需求</span><span class="sxs-lookup"><span data-stu-id="6f364-117">Requirement</span></span> | <span data-ttu-id="6f364-118">值</span><span class="sxs-lookup"><span data-stu-id="6f364-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f364-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f364-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f364-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f364-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f364-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f364-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f364-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f364-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f364-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6f364-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f364-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f364-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





