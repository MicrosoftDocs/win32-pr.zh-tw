---
title: 'LVM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 取得清單視圖控制項的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ GetBkColor 宏來傳送。
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- LVM_GETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464285"
---
# <a name="lvm_getbkcolor-message"></a><span data-ttu-id="2c480-105">LVM \_ GETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="2c480-105">LVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="2c480-106">取得清單視圖控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="2c480-106">Gets the background color of a list-view control.</span></span> <span data-ttu-id="2c480-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="2c480-107">You can send this message explicitly or by using the [**ListView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c480-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c480-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c480-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c480-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2c480-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2c480-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2c480-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c480-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2c480-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2c480-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c480-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c480-113">Return value</span></span>

<span data-ttu-id="2c480-114">傳回清單視圖控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="2c480-114">Returns the background color of the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c480-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c480-115">Requirements</span></span>



| <span data-ttu-id="2c480-116">需求</span><span class="sxs-lookup"><span data-stu-id="2c480-116">Requirement</span></span> | <span data-ttu-id="2c480-117">值</span><span class="sxs-lookup"><span data-stu-id="2c480-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c480-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c480-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c480-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c480-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c480-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c480-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c480-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c480-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c480-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2c480-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c480-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c480-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





