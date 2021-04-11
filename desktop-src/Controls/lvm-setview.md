---
title: 'LVM_SETVIEW 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的視圖。
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105462"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="dd8d1-104">LVM \_ SETVIEW 訊息</span><span class="sxs-lookup"><span data-stu-id="dd8d1-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="dd8d1-105">設定清單視圖控制項的視圖。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd8d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd8d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd8d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd8d1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dd8d1-108">指定視圖的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="dd8d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd8d1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd8d1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd8d1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd8d1-111">Return value</span></span>

<span data-ttu-id="dd8d1-112">如果成功，則傳回1，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="dd8d1-113">例如，如果視圖無效，則會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd8d1-114">備註</span><span class="sxs-lookup"><span data-stu-id="dd8d1-114">Remarks</span></span>

<span data-ttu-id="dd8d1-115">以下是 views 的值。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-115">Following are the values for views.</span></span>

-   <span data-ttu-id="dd8d1-116">LV \_ 視圖 \_ 詳細資料</span><span class="sxs-lookup"><span data-stu-id="dd8d1-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="dd8d1-117">LV \_ 視圖 \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="dd8d1-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="dd8d1-118">LV \_ 視圖 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="dd8d1-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="dd8d1-119">LV \_ 視圖 \_ SMALLICON</span><span class="sxs-lookup"><span data-stu-id="dd8d1-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="dd8d1-120">LV \_ 視圖 \_ 磚</span><span class="sxs-lookup"><span data-stu-id="dd8d1-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="dd8d1-121">若要使用此訊息，您必須提供指定 Comctl32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="dd8d1-122">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="dd8d1-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd8d1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd8d1-123">Requirements</span></span>



| <span data-ttu-id="dd8d1-124">需求</span><span class="sxs-lookup"><span data-stu-id="dd8d1-124">Requirement</span></span> | <span data-ttu-id="dd8d1-125">值</span><span class="sxs-lookup"><span data-stu-id="dd8d1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd8d1-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd8d1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dd8d1-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd8d1-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd8d1-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd8d1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dd8d1-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd8d1-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd8d1-130">標頭</span><span class="sxs-lookup"><span data-stu-id="dd8d1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd8d1-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd8d1-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





