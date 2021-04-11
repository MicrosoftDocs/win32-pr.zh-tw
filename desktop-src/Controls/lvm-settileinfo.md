---
title: 'LVM_SETTILEINFO 訊息 (Commctrl .h) '
description: 設定清單視圖控制項之現有磚的資訊。
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- LVM_SETTILEINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094303"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="a60d7-104">LVM \_ SETTILEINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="a60d7-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="a60d7-105">設定清單視圖控制項之現有磚的資訊。</span><span class="sxs-lookup"><span data-stu-id="a60d7-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a60d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="a60d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60d7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a60d7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a60d7-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a60d7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a60d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a60d7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a60d7-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a>結構的指標，其中包含要設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="a60d7-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a60d7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a60d7-111">Return value</span></span>

<span data-ttu-id="a60d7-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a60d7-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a60d7-113">備註</span><span class="sxs-lookup"><span data-stu-id="a60d7-113">Remarks</span></span>

<span data-ttu-id="a60d7-114">**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 SETTILEINFO。</span><span class="sxs-lookup"><span data-stu-id="a60d7-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="a60d7-115">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="a60d7-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a60d7-116">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="a60d7-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a60d7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a60d7-117">Requirements</span></span>



| <span data-ttu-id="a60d7-118">需求</span><span class="sxs-lookup"><span data-stu-id="a60d7-118">Requirement</span></span> | <span data-ttu-id="a60d7-119">值</span><span class="sxs-lookup"><span data-stu-id="a60d7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a60d7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a60d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a60d7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a60d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a60d7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a60d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a60d7-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a60d7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a60d7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a60d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a60d7-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a60d7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





