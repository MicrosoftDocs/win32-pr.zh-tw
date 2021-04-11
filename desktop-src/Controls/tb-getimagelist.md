---
title: 'TB_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取工具列控制項用來顯示其預設狀態之按鈕的影像清單。 當按鈕未熱或停用時，工具列控制項會使用此影像清單來顯示按鈕。
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685601"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="f4a54-105">TB \_ GETIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="f4a54-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="f4a54-106">抓取工具列控制項用來顯示其預設狀態之按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="f4a54-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="f4a54-107">當按鈕未熱或停用時，工具列控制項會使用此影像清單來顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="f4a54-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4a54-108">參數</span><span class="sxs-lookup"><span data-stu-id="f4a54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4a54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4a54-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f4a54-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4a54-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4a54-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4a54-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f4a54-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a54-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4a54-113">Return value</span></span>

<span data-ttu-id="f4a54-114">傳回影像清單的控制碼，如果未設定影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="f4a54-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a54-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4a54-115">Requirements</span></span>



| <span data-ttu-id="f4a54-116">需求</span><span class="sxs-lookup"><span data-stu-id="f4a54-116">Requirement</span></span> | <span data-ttu-id="f4a54-117">值</span><span class="sxs-lookup"><span data-stu-id="f4a54-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a54-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4a54-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a54-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4a54-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4a54-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4a54-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a54-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4a54-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4a54-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f4a54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4a54-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a54-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





