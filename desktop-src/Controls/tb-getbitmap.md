---
title: 'TB_GETBITMAP 訊息 (Commctrl .h) '
description: 抓取與工具列中的按鈕相關聯的點陣圖索引。
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- TB_GETBITMAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935158"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="ae27b-104">TB \_ GETBITMAP 訊息</span><span class="sxs-lookup"><span data-stu-id="ae27b-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="ae27b-105">抓取與工具列中的按鈕相關聯的點陣圖索引。</span><span class="sxs-lookup"><span data-stu-id="ae27b-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae27b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae27b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae27b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae27b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae27b-108">要取出其點陣圖索引之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae27b-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="ae27b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae27b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae27b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ae27b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae27b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae27b-111">Return value</span></span>

<span data-ttu-id="ae27b-112">如果成功，則傳回點陣圖的索引，否則為零。</span><span class="sxs-lookup"><span data-stu-id="ae27b-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae27b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae27b-113">Requirements</span></span>



| <span data-ttu-id="ae27b-114">需求</span><span class="sxs-lookup"><span data-stu-id="ae27b-114">Requirement</span></span> | <span data-ttu-id="ae27b-115">值</span><span class="sxs-lookup"><span data-stu-id="ae27b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae27b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae27b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ae27b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae27b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae27b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae27b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ae27b-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae27b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae27b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ae27b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae27b-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae27b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





