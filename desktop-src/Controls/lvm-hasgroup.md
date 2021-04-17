---
title: 'LVM_HASGROUP 訊息 (Commctrl .h) '
description: 判斷清單視圖控制項是否有指定的群組。
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466497"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="88892-104">LVM \_ HASGROUP 訊息</span><span class="sxs-lookup"><span data-stu-id="88892-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="88892-105">判斷清單視圖控制項是否有指定的群組。</span><span class="sxs-lookup"><span data-stu-id="88892-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="88892-106">參數</span><span class="sxs-lookup"><span data-stu-id="88892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88892-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88892-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="88892-108">群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88892-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="88892-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88892-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="88892-110">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="88892-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88892-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="88892-111">Return value</span></span>

<span data-ttu-id="88892-112">如果清單視圖控制項具有指定的群組，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="88892-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="88892-113">備註</span><span class="sxs-lookup"><span data-stu-id="88892-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88892-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="88892-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="88892-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="88892-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88892-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="88892-116">Requirements</span></span>



| <span data-ttu-id="88892-117">需求</span><span class="sxs-lookup"><span data-stu-id="88892-117">Requirement</span></span> | <span data-ttu-id="88892-118">值</span><span class="sxs-lookup"><span data-stu-id="88892-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88892-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88892-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88892-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88892-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88892-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88892-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88892-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88892-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88892-123">標頭</span><span class="sxs-lookup"><span data-stu-id="88892-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="88892-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="88892-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





