---
title: 'RB_DELETEBAND 訊息 (Commctrl .h) '
description: 從 Rebar 控制項刪除頻外。
ms.assetid: 15f2ea78-5c3f-4fe1-a020-025c33f00703
keywords:
- RB_DELETEBAND message Windows 控制項
topic_type:
- apiref
api_name:
- RB_DELETEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fd8593c816b64f0d7f82058b3779f256dd521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966329"
---
# <a name="rb_deleteband-message"></a><span data-ttu-id="42f07-104">RB \_ DELETEBAND 訊息</span><span class="sxs-lookup"><span data-stu-id="42f07-104">RB\_DELETEBAND message</span></span>

<span data-ttu-id="42f07-105">從 Rebar 控制項刪除頻外。</span><span class="sxs-lookup"><span data-stu-id="42f07-105">Deletes a band from a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="42f07-106">參數</span><span class="sxs-lookup"><span data-stu-id="42f07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42f07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42f07-108">要刪除之帶狀線的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="42f07-108">Zero-based index of the band to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="42f07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42f07-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="42f07-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="42f07-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="42f07-111">Return value</span></span>

<span data-ttu-id="42f07-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="42f07-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f07-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="42f07-113">Requirements</span></span>



| <span data-ttu-id="42f07-114">需求</span><span class="sxs-lookup"><span data-stu-id="42f07-114">Requirement</span></span> | <span data-ttu-id="42f07-115">值</span><span class="sxs-lookup"><span data-stu-id="42f07-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42f07-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42f07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42f07-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42f07-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42f07-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42f07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42f07-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42f07-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42f07-120">標頭</span><span class="sxs-lookup"><span data-stu-id="42f07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f07-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="42f07-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





