---
title: 'IPM_SETFOCUS 訊息 (Commctrl .h) '
description: 將鍵盤焦點設定為 IP 位址控制項中的指定欄位。 將會選取該欄位中的所有文字。
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d713e0a8b7eb838a2db5c4738c801d4fb76b782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104460"
---
# <a name="ipm_setfocus-message"></a><span data-ttu-id="37c45-105">IPM \_ SETFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="37c45-105">IPM\_SETFOCUS message</span></span>

<span data-ttu-id="37c45-106">將鍵盤焦點設定為 IP 位址控制項中的指定欄位。</span><span class="sxs-lookup"><span data-stu-id="37c45-106">Sets the keyboard focus to the specified field in the IP address control.</span></span> <span data-ttu-id="37c45-107">將會選取該欄位中的所有文字。</span><span class="sxs-lookup"><span data-stu-id="37c45-107">All of the text in that field will be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="37c45-108">參數</span><span class="sxs-lookup"><span data-stu-id="37c45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37c45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37c45-110">以零為基底的欄位索引，應設定焦點。</span><span class="sxs-lookup"><span data-stu-id="37c45-110">A zero-based field index to which the focus should be set.</span></span> <span data-ttu-id="37c45-111">如果這個值大於欄位數目，則焦點會設定為第一個空白欄位。</span><span class="sxs-lookup"><span data-stu-id="37c45-111">If this value is greater than the number of fields, focus is set to the first blank field.</span></span> <span data-ttu-id="37c45-112">如果所有欄位都是非空白的，則焦點會設定為第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="37c45-112">If all fields are nonblank, focus is set to the first field.</span></span>

</dd> <dt>

<span data-ttu-id="37c45-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37c45-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="37c45-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="37c45-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c45-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="37c45-115">Return value</span></span>

<span data-ttu-id="37c45-116">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="37c45-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="37c45-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="37c45-117">Requirements</span></span>



| <span data-ttu-id="37c45-118">需求</span><span class="sxs-lookup"><span data-stu-id="37c45-118">Requirement</span></span> | <span data-ttu-id="37c45-119">值</span><span class="sxs-lookup"><span data-stu-id="37c45-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37c45-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37c45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="37c45-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37c45-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37c45-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37c45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="37c45-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37c45-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37c45-124">標頭</span><span class="sxs-lookup"><span data-stu-id="37c45-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="37c45-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="37c45-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





