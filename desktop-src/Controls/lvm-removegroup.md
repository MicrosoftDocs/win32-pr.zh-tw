---
title: 'LVM_REMOVEGROUP 訊息 (Commctrl .h) '
description: 從清單視圖控制項移除群組。
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934629"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="ad12c-104">LVM \_ REMOVEGROUP 訊息</span><span class="sxs-lookup"><span data-stu-id="ad12c-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="ad12c-105">從清單視圖控制項移除群組。</span><span class="sxs-lookup"><span data-stu-id="ad12c-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad12c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad12c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad12c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad12c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ad12c-108">指定要移除之群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad12c-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="ad12c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad12c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad12c-110">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ad12c-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad12c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad12c-111">Return value</span></span>

<span data-ttu-id="ad12c-112">如果成功，則傳回群組的索引，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="ad12c-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad12c-113">備註</span><span class="sxs-lookup"><span data-stu-id="ad12c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad12c-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="ad12c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ad12c-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ad12c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad12c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad12c-116">Requirements</span></span>



| <span data-ttu-id="ad12c-117">需求</span><span class="sxs-lookup"><span data-stu-id="ad12c-117">Requirement</span></span> | <span data-ttu-id="ad12c-118">值</span><span class="sxs-lookup"><span data-stu-id="ad12c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad12c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad12c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad12c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad12c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad12c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad12c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad12c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad12c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad12c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ad12c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad12c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad12c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





