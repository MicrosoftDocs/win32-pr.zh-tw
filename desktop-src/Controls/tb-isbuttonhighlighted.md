---
title: 'TB_ISBUTTONHIGHLIGHTED 訊息 (Commctrl .h) '
description: 檢查工具列按鈕的醒目提示狀態。
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- TB_ISBUTTONHIGHLIGHTED message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024852"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="3ed70-104">TB \_ ISBUTTONHIGHLIGHTED 訊息</span><span class="sxs-lookup"><span data-stu-id="3ed70-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="3ed70-105">檢查工具列按鈕的醒目提示狀態。</span><span class="sxs-lookup"><span data-stu-id="3ed70-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ed70-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ed70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ed70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ed70-108">工具列按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ed70-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="3ed70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ed70-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3ed70-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3ed70-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed70-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ed70-111">Return value</span></span>

<span data-ttu-id="3ed70-112">如果按鈕已反白顯示，則會傳回非零，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3ed70-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed70-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ed70-113">Requirements</span></span>



| <span data-ttu-id="3ed70-114">需求</span><span class="sxs-lookup"><span data-stu-id="3ed70-114">Requirement</span></span> | <span data-ttu-id="3ed70-115">值</span><span class="sxs-lookup"><span data-stu-id="3ed70-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed70-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ed70-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed70-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ed70-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ed70-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ed70-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed70-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ed70-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ed70-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3ed70-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ed70-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed70-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





