---
title: 'TB_SETANCHORHIGHLIGHT 訊息 (Commctrl .h) '
description: 設定工具列的錨點醒目提示設定。
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- TB_SETANCHORHIGHLIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967712"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="1dd09-104">TB \_ SETANCHORHIGHLIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="1dd09-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="1dd09-105">設定工具列的錨點醒目提示設定。</span><span class="sxs-lookup"><span data-stu-id="1dd09-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dd09-106">參數</span><span class="sxs-lookup"><span data-stu-id="1dd09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd09-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dd09-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd09-108">**布林** 值，指定是否啟用或停用錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1dd09-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="1dd09-109">如果此值為非零值，則會啟用錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1dd09-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="1dd09-110">如果此值為零，將會停用錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1dd09-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1dd09-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dd09-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1dd09-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1dd09-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd09-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1dd09-113">Return value</span></span>

<span data-ttu-id="1dd09-114">傳回上一個錨點醒目提示設定。</span><span class="sxs-lookup"><span data-stu-id="1dd09-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="1dd09-115">如果此值為非零值，則會啟用錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1dd09-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="1dd09-116">如果此值為零，則會停用錨點反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1dd09-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd09-117">備註</span><span class="sxs-lookup"><span data-stu-id="1dd09-117">Remarks</span></span>

<span data-ttu-id="1dd09-118">工具列中的錨點醒目提示表示最後一個反白顯示的專案會保持反白顯示，直到另一個專案反白顯示。</span><span class="sxs-lookup"><span data-stu-id="1dd09-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="1dd09-119">即使游標離開工具列控制項，也會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="1dd09-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dd09-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dd09-120">Requirements</span></span>



| <span data-ttu-id="1dd09-121">需求</span><span class="sxs-lookup"><span data-stu-id="1dd09-121">Requirement</span></span> | <span data-ttu-id="1dd09-122">值</span><span class="sxs-lookup"><span data-stu-id="1dd09-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd09-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dd09-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd09-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dd09-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1dd09-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dd09-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd09-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dd09-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dd09-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1dd09-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd09-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd09-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





