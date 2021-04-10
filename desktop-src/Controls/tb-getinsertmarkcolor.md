---
title: 'TB_GETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 抓取用來繪製工具列之插入標記的色彩。
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- TB_GETINSERTMARKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ceebd5f3989ed870cf70ccad819300d85c05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843608"
---
# <a name="tb_getinsertmarkcolor-message"></a><span data-ttu-id="865ac-104">TB \_ GETINSERTMARKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="865ac-104">TB\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="865ac-105">抓取用來繪製工具列之插入標記的色彩。</span><span class="sxs-lookup"><span data-stu-id="865ac-105">Retrieves the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="865ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="865ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="865ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="865ac-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="865ac-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="865ac-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="865ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="865ac-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="865ac-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="865ac-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="865ac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="865ac-111">Return value</span></span>

<span data-ttu-id="865ac-112">傳回包含目前插入標記色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="865ac-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="865ac-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="865ac-113">Requirements</span></span>



| <span data-ttu-id="865ac-114">需求</span><span class="sxs-lookup"><span data-stu-id="865ac-114">Requirement</span></span> | <span data-ttu-id="865ac-115">值</span><span class="sxs-lookup"><span data-stu-id="865ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="865ac-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="865ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="865ac-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="865ac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="865ac-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="865ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="865ac-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="865ac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="865ac-120">標頭</span><span class="sxs-lookup"><span data-stu-id="865ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="865ac-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="865ac-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="865ac-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="865ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="865ac-123">**TB \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="865ac-123">**TB\_SETINSERTMARKCOLOR**</span></span>](tb-setinsertmarkcolor.md)
</dt> </dl>

 

