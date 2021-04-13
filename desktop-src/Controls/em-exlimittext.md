---
title: 'EM_EXLIMITTEXT 訊息 (Richedit .h) '
description: 將使用者可以輸入或貼上的文字數量上限設定為 rich edit 控制項。
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465896"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="ea9a1-104">EM \_ EXLIMITTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="ea9a1-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="ea9a1-105">將使用者可以輸入或貼上的文字數量上限設定為 rich edit 控制項。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea9a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="ea9a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea9a1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9a1-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea9a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea9a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9a1-110">指定可以輸入的最大文字數量。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="ea9a1-111">如果此參數為零，則會使用預設的最大值，也就是64K 個字元。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="ea9a1-112">COM 物件會計算為單一字元。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9a1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea9a1-113">Return value</span></span>

<span data-ttu-id="ea9a1-114">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9a1-115">備註</span><span class="sxs-lookup"><span data-stu-id="ea9a1-115">Remarks</span></span>

<span data-ttu-id="ea9a1-116">**Em \_ EXLIMITTEXT** 訊息所設定的文字限制不會限制您可以使用 [**Em \_ STREAMIN**](em-streamin.md)訊息將 *lParam* 設定為 SF text 來串流至 rich edit 控制項的文字數量 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="ea9a1-117">不過，它會限制您可以使用 **EM \_ STREAMIN** 訊息，將 *lParam* 設定為 SF rtf，以串流至 rich edit 控制項的文字數量 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="ea9a1-118">在呼叫 **EM \_ EXLIMITTEXT** 之前，使用者可以輸入的文字數量預設限制為32767個字元。</span><span class="sxs-lookup"><span data-stu-id="ea9a1-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9a1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea9a1-119">Requirements</span></span>



| <span data-ttu-id="ea9a1-120">需求</span><span class="sxs-lookup"><span data-stu-id="ea9a1-120">Requirement</span></span> | <span data-ttu-id="ea9a1-121">值</span><span class="sxs-lookup"><span data-stu-id="ea9a1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9a1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea9a1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9a1-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea9a1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea9a1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea9a1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9a1-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea9a1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea9a1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ea9a1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9a1-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea9a1-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9a1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea9a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9a1-129">**EM \_ STREAMIN**</span><span class="sxs-lookup"><span data-stu-id="ea9a1-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





