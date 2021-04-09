---
title: 'TB_GETDISABLEDIMAGELIST 訊息 (Commctrl .h) '
description: 抓取工具列控制項用來顯示非作用中按鈕的影像清單。
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- TB_GETDISABLEDIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934268"
---
# <a name="tb_getdisabledimagelist-message"></a><span data-ttu-id="c5209-104">TB \_ GETDISABLEDIMAGELIST 訊息</span><span class="sxs-lookup"><span data-stu-id="c5209-104">TB\_GETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="c5209-105">抓取工具列控制項用來顯示非作用中按鈕的影像清單。</span><span class="sxs-lookup"><span data-stu-id="c5209-105">Retrieves the image list that a toolbar control uses to display inactive buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5209-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5209-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5209-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5209-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5209-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c5209-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c5209-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5209-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c5209-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c5209-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5209-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5209-111">Return value</span></span>

<span data-ttu-id="c5209-112">傳回非使用中影像清單的控制碼，如果未設定任何非使用中的影像清單，則傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c5209-112">Returns the handle to the inactive image list, or **NULL** if no inactive image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5209-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5209-113">Requirements</span></span>



| <span data-ttu-id="c5209-114">需求</span><span class="sxs-lookup"><span data-stu-id="c5209-114">Requirement</span></span> | <span data-ttu-id="c5209-115">值</span><span class="sxs-lookup"><span data-stu-id="c5209-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5209-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5209-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c5209-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5209-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5209-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5209-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c5209-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5209-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5209-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c5209-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5209-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5209-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





