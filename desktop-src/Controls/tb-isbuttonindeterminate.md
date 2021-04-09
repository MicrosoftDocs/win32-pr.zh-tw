---
title: 'TB_ISBUTTONINDETERMINATE 訊息 (Commctrl .h) '
description: 判斷工具列中指定的按鈕是否不定。
ms.assetid: b4d759b3-cdbc-417b-9da4-4ed9edc38c0e
keywords:
- TB_ISBUTTONINDETERMINATE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONINDETERMINATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc024efcad9f0f48ae4882b019269903c249bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024851"
---
# <a name="tb_isbuttonindeterminate-message"></a><span data-ttu-id="2a3c3-104">TB \_ ISBUTTONINDETERMINATE 訊息</span><span class="sxs-lookup"><span data-stu-id="2a3c3-104">TB\_ISBUTTONINDETERMINATE message</span></span>

<span data-ttu-id="2a3c3-105">判斷工具列中指定的按鈕是否不定。</span><span class="sxs-lookup"><span data-stu-id="2a3c3-105">Determines whether the specified button in a toolbar is indeterminate.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a3c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a3c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a3c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a3c3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a3c3-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a3c3-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="2a3c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a3c3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2a3c3-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2a3c3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a3c3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a3c3-111">Return value</span></span>

<span data-ttu-id="2a3c3-112">如果按鈕是不定的，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="2a3c3-112">Returns nonzero if the button is indeterminate, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3c3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a3c3-113">Requirements</span></span>



| <span data-ttu-id="2a3c3-114">需求</span><span class="sxs-lookup"><span data-stu-id="2a3c3-114">Requirement</span></span> | <span data-ttu-id="2a3c3-115">值</span><span class="sxs-lookup"><span data-stu-id="2a3c3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3c3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a3c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3c3-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a3c3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a3c3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a3c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3c3-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a3c3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a3c3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2a3c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3c3-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





