---
title: 'TB_SETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 設定用來繪製工具列之插入標記的色彩。
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093815"
---
# <a name="tb_setinsertmarkcolor-message"></a><span data-ttu-id="f9201-104">TB \_ SETINSERTMARKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="f9201-104">TB\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="f9201-105">設定用來繪製工具列之插入標記的色彩。</span><span class="sxs-lookup"><span data-stu-id="f9201-105">Sets the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9201-106">參數</span><span class="sxs-lookup"><span data-stu-id="f9201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9201-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9201-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f9201-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f9201-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f9201-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9201-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9201-110">**COLORREF** 值，其中包含新的插入標記色彩。</span><span class="sxs-lookup"><span data-stu-id="f9201-110">**COLORREF** value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9201-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f9201-111">Return value</span></span>

<span data-ttu-id="f9201-112">傳回包含先前插入標記色彩的 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="f9201-112">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9201-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9201-113">Requirements</span></span>



| <span data-ttu-id="f9201-114">需求</span><span class="sxs-lookup"><span data-stu-id="f9201-114">Requirement</span></span> | <span data-ttu-id="f9201-115">值</span><span class="sxs-lookup"><span data-stu-id="f9201-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9201-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9201-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f9201-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9201-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9201-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9201-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f9201-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9201-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9201-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f9201-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9201-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9201-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9201-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9201-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9201-123">**TB \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="f9201-123">**TB\_GETINSERTMARKCOLOR**</span></span>](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





