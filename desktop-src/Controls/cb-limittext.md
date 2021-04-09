---
title: 'CB_LIMITTEXT 訊息 (Winuser .h) '
description: 限制使用者可在下拉式方塊的編輯控制項中輸入的文字長度。
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025083"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="63990-104">CB \_ LIMITTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="63990-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="63990-105">限制使用者可在下拉式方塊的編輯控制項中輸入的文字長度。</span><span class="sxs-lookup"><span data-stu-id="63990-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="63990-106">參數</span><span class="sxs-lookup"><span data-stu-id="63990-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63990-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63990-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63990-108">使用者可以輸入的最大 **TCHARs** 數目，不包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="63990-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="63990-109">如果此參數為零，則文字長度限制為0x7FFFFFFE 字元。</span><span class="sxs-lookup"><span data-stu-id="63990-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="63990-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63990-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63990-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="63990-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63990-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="63990-112">Return value</span></span>

<span data-ttu-id="63990-113">傳回值一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="63990-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="63990-114">備註</span><span class="sxs-lookup"><span data-stu-id="63990-114">Remarks</span></span>

<span data-ttu-id="63990-115">如果下拉式方塊沒有 [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) 樣式，將文字限制設定為大於編輯控制項的大小不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="63990-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="63990-116">**CB \_ LIMITTEXT** 郵件只會限制使用者可以輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="63990-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="63990-117">當傳送訊息時，它不會影響任何已在編輯控制項中的文字，也不會影響選取清單方塊中的字串時，複製到編輯控制項的文字長度。</span><span class="sxs-lookup"><span data-stu-id="63990-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="63990-118">使用者可以在編輯控制項中輸入的文字預設限制為 30000 **TCHARs**。</span><span class="sxs-lookup"><span data-stu-id="63990-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="63990-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="63990-119">Requirements</span></span>



| <span data-ttu-id="63990-120">需求</span><span class="sxs-lookup"><span data-stu-id="63990-120">Requirement</span></span> | <span data-ttu-id="63990-121">值</span><span class="sxs-lookup"><span data-stu-id="63990-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63990-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63990-122">Minimum supported client</span></span><br/> | <span data-ttu-id="63990-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63990-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63990-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63990-124">Minimum supported server</span></span><br/> | <span data-ttu-id="63990-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63990-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63990-126">標頭</span><span class="sxs-lookup"><span data-stu-id="63990-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="63990-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="63990-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





