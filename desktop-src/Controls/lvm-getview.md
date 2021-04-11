---
title: 'LVM_GETVIEW 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的目前視圖。
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105485"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="763e4-104">LVM \_ GETVIEW 訊息</span><span class="sxs-lookup"><span data-stu-id="763e4-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="763e4-105">抓取清單視圖控制項的目前視圖。</span><span class="sxs-lookup"><span data-stu-id="763e4-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="763e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="763e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="763e4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="763e4-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="763e4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="763e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="763e4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="763e4-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="763e4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="763e4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="763e4-111">Return value</span></span>

<span data-ttu-id="763e4-112">傳回指定目前視圖的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="763e4-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="763e4-113">備註</span><span class="sxs-lookup"><span data-stu-id="763e4-113">Remarks</span></span>

<span data-ttu-id="763e4-114">以下是 views 的值。</span><span class="sxs-lookup"><span data-stu-id="763e4-114">Following are the values for views.</span></span>

-   <span data-ttu-id="763e4-115">LV \_ 視圖 \_ 詳細資料</span><span class="sxs-lookup"><span data-stu-id="763e4-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="763e4-116">LV \_ 視圖 \_ 圖示</span><span class="sxs-lookup"><span data-stu-id="763e4-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="763e4-117">LV \_ 視圖 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="763e4-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="763e4-118">LV \_ 視圖 \_ SMALLICON</span><span class="sxs-lookup"><span data-stu-id="763e4-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="763e4-119">LV \_ 視圖 \_ 磚</span><span class="sxs-lookup"><span data-stu-id="763e4-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="763e4-120">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="763e4-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="763e4-121">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="763e4-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="763e4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="763e4-122">Requirements</span></span>



| <span data-ttu-id="763e4-123">需求</span><span class="sxs-lookup"><span data-stu-id="763e4-123">Requirement</span></span> | <span data-ttu-id="763e4-124">值</span><span class="sxs-lookup"><span data-stu-id="763e4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="763e4-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="763e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="763e4-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="763e4-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="763e4-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="763e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="763e4-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="763e4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="763e4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="763e4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="763e4-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="763e4-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





