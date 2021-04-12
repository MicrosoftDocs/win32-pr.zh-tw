---
title: 'LVM_SETGROUPMETRICS 訊息 (Commctrl .h) '
description: 設定群組顯示的相關資訊。
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- LVM_SETGROUPMETRICS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317116"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="5cba2-104">LVM \_ SETGROUPMETRICS 訊息</span><span class="sxs-lookup"><span data-stu-id="5cba2-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="5cba2-105">設定群組顯示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5cba2-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cba2-106">參數</span><span class="sxs-lookup"><span data-stu-id="5cba2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cba2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cba2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5cba2-108">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5cba2-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="5cba2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cba2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5cba2-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a>結構的指標，其中包含要設定的度量。</span><span class="sxs-lookup"><span data-stu-id="5cba2-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cba2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cba2-111">Return value</span></span>

<span data-ttu-id="5cba2-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="5cba2-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cba2-113">備註</span><span class="sxs-lookup"><span data-stu-id="5cba2-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5cba2-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="5cba2-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5cba2-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5cba2-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5cba2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cba2-116">Requirements</span></span>



| <span data-ttu-id="5cba2-117">需求</span><span class="sxs-lookup"><span data-stu-id="5cba2-117">Requirement</span></span> | <span data-ttu-id="5cba2-118">值</span><span class="sxs-lookup"><span data-stu-id="5cba2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cba2-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cba2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5cba2-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cba2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cba2-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cba2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5cba2-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cba2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cba2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5cba2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cba2-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5cba2-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





