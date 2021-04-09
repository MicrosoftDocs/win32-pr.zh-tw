---
title: 'LVM_SETTILEVIEWINFO 訊息 (Commctrl .h) '
description: 設定清單視圖控制項在並排顯示中使用的資訊。
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- LVM_SETTILEVIEWINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094300"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="41494-104">LVM \_ SETTILEVIEWINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="41494-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="41494-105">設定清單視圖控制項在並排顯示中使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="41494-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="41494-106">參數</span><span class="sxs-lookup"><span data-stu-id="41494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41494-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41494-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41494-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="41494-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41494-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41494-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="41494-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a>結構的指標，其中包含要設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="41494-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41494-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="41494-111">Return value</span></span>

<span data-ttu-id="41494-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="41494-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41494-113">備註</span><span class="sxs-lookup"><span data-stu-id="41494-113">Remarks</span></span>

<span data-ttu-id="41494-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="41494-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="41494-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="41494-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41494-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="41494-116">Requirements</span></span>



| <span data-ttu-id="41494-117">需求</span><span class="sxs-lookup"><span data-stu-id="41494-117">Requirement</span></span> | <span data-ttu-id="41494-118">值</span><span class="sxs-lookup"><span data-stu-id="41494-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41494-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41494-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41494-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41494-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41494-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41494-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41494-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41494-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41494-123">標頭</span><span class="sxs-lookup"><span data-stu-id="41494-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41494-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="41494-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





