---
title: 'TB_GETBUTTONSIZE 訊息 (Commctrl .h) '
description: 抓取工具列按鈕目前的寬度和高度（以圖元為單位）。
ms.assetid: c1b72494-670b-4cf8-a78f-c67b6eee0677
keywords:
- TB_GETBUTTONSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a414f5b338353d7d8ce22a081e9b711a2b56a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844447"
---
# <a name="tb_getbuttonsize-message"></a><span data-ttu-id="f984a-104">TB \_ GETBUTTONSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="f984a-104">TB\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="f984a-105">抓取工具列按鈕目前的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f984a-105">Retrieves the current width and height of toolbar buttons, in pixels.</span></span>

## <a name="parameters"></a><span data-ttu-id="f984a-106">參數</span><span class="sxs-lookup"><span data-stu-id="f984a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f984a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f984a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f984a-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f984a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f984a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f984a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f984a-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f984a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f984a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f984a-111">Return value</span></span>

<span data-ttu-id="f984a-112">傳回 **DWORD** 值，其中包含低字和高單字中的寬度和高度值。</span><span class="sxs-lookup"><span data-stu-id="f984a-112">Returns a **DWORD** value that contains the width and height values in the low word and high word, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="f984a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f984a-113">Requirements</span></span>



| <span data-ttu-id="f984a-114">需求</span><span class="sxs-lookup"><span data-stu-id="f984a-114">Requirement</span></span> | <span data-ttu-id="f984a-115">值</span><span class="sxs-lookup"><span data-stu-id="f984a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f984a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f984a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f984a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f984a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f984a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f984a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f984a-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f984a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f984a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f984a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f984a-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f984a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





