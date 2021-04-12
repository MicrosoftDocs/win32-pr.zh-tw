---
title: 'TB_DELETEBUTTON 訊息 (Commctrl .h) '
description: 從工具列中刪除按鈕。
ms.assetid: 6ba569f0-c400-4c0d-bc9f-3a82bcef0360
keywords:
- TB_DELETEBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TB_DELETEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d9bbbca143351f70005990b5ac97fa4fa35cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935159"
---
# <a name="tb_deletebutton-message"></a><span data-ttu-id="fbeaa-104">TB \_ DELETEBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="fbeaa-104">TB\_DELETEBUTTON message</span></span>

<span data-ttu-id="fbeaa-105">從工具列中刪除按鈕。</span><span class="sxs-lookup"><span data-stu-id="fbeaa-105">Deletes a button from the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbeaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbeaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbeaa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbeaa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbeaa-108">要刪除的按鈕之以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="fbeaa-108">Zero-based index of the button to delete.</span></span>

</dd> <dt>

<span data-ttu-id="fbeaa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbeaa-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fbeaa-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fbeaa-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbeaa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbeaa-111">Return value</span></span>

<span data-ttu-id="fbeaa-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="fbeaa-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbeaa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbeaa-113">Requirements</span></span>



| <span data-ttu-id="fbeaa-114">需求</span><span class="sxs-lookup"><span data-stu-id="fbeaa-114">Requirement</span></span> | <span data-ttu-id="fbeaa-115">值</span><span class="sxs-lookup"><span data-stu-id="fbeaa-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbeaa-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbeaa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fbeaa-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbeaa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbeaa-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbeaa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fbeaa-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbeaa-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbeaa-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fbeaa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbeaa-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbeaa-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





