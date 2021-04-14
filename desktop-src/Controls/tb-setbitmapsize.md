---
title: 'TB_SETBITMAPSIZE 訊息 (Commctrl .h) '
description: 設定要新增至工具列之點陣圖影像的大小。
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464256"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="76e34-104">TB \_ SETBITMAPSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="76e34-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="76e34-105">設定要新增至工具列之點陣圖影像的大小。</span><span class="sxs-lookup"><span data-stu-id="76e34-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="76e34-106">參數</span><span class="sxs-lookup"><span data-stu-id="76e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76e34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76e34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76e34-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="76e34-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="76e34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76e34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76e34-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定點陣圖影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="76e34-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="76e34-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定點陣圖影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="76e34-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76e34-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="76e34-112">Return value</span></span>

<span data-ttu-id="76e34-113">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="76e34-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="76e34-114">備註</span><span class="sxs-lookup"><span data-stu-id="76e34-114">Remarks</span></span>

<span data-ttu-id="76e34-115">只有在將任何點陣圖新增至工具列之後，才可以設定大小。</span><span class="sxs-lookup"><span data-stu-id="76e34-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="76e34-116">如果應用程式未明確設定點陣圖大小，則大小預設為 16 x 15 圖元。</span><span class="sxs-lookup"><span data-stu-id="76e34-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="76e34-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="76e34-117">Requirements</span></span>



| <span data-ttu-id="76e34-118">需求</span><span class="sxs-lookup"><span data-stu-id="76e34-118">Requirement</span></span> | <span data-ttu-id="76e34-119">值</span><span class="sxs-lookup"><span data-stu-id="76e34-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76e34-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76e34-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76e34-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76e34-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76e34-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76e34-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76e34-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76e34-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76e34-124">標頭</span><span class="sxs-lookup"><span data-stu-id="76e34-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76e34-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="76e34-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

