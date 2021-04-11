---
title: 'SB_GETICON 訊息 (Commctrl .h) '
description: 抓取狀態列中元件的圖示。
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- SB_GETICON message Windows 控制項
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844003"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="bacbd-104">SB \_ GETICON 訊息</span><span class="sxs-lookup"><span data-stu-id="bacbd-104">SB\_GETICON message</span></span>

<span data-ttu-id="bacbd-105">抓取狀態列中元件的圖示。</span><span class="sxs-lookup"><span data-stu-id="bacbd-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bacbd-106">參數</span><span class="sxs-lookup"><span data-stu-id="bacbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bacbd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bacbd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bacbd-108">元件以零為起始的索引，其中包含要取出的圖示。</span><span class="sxs-lookup"><span data-stu-id="bacbd-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="bacbd-109">如果此參數為-1，則會假設狀態列為 [簡單模式](status-bars.md) 的狀態列。</span><span class="sxs-lookup"><span data-stu-id="bacbd-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="bacbd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bacbd-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bacbd-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="bacbd-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bacbd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bacbd-112">Return value</span></span>

<span data-ttu-id="bacbd-113">如果成功，則傳回圖示的控制碼; 否則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bacbd-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bacbd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bacbd-114">Requirements</span></span>



| <span data-ttu-id="bacbd-115">需求</span><span class="sxs-lookup"><span data-stu-id="bacbd-115">Requirement</span></span> | <span data-ttu-id="bacbd-116">值</span><span class="sxs-lookup"><span data-stu-id="bacbd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bacbd-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bacbd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bacbd-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bacbd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bacbd-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bacbd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bacbd-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bacbd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bacbd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bacbd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bacbd-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bacbd-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





