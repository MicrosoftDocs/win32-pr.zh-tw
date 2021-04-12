---
title: 'EM_GETIMEMODEBIAS 訊息 (Richedit .h) '
description: 抓取 Microsoft Rich Edit 控制項的輸入方法編輯器 (IME) 模式偏差。
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025292"
---
# <a name="em_getimemodebias-message"></a><span data-ttu-id="64d63-104">EM \_ GETIMEMODEBIAS 訊息</span><span class="sxs-lookup"><span data-stu-id="64d63-104">EM\_GETIMEMODEBIAS message</span></span>

<span data-ttu-id="64d63-105">抓取 Microsoft Rich Edit 控制項的輸入方法編輯器 (IME) 模式偏差。</span><span class="sxs-lookup"><span data-stu-id="64d63-105">Retrieves the Input Method Editor (IME) mode bias for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="64d63-106">參數</span><span class="sxs-lookup"><span data-stu-id="64d63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d63-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64d63-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d63-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="64d63-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="64d63-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64d63-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d63-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="64d63-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d63-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="64d63-111">Return value</span></span>

<span data-ttu-id="64d63-112">此訊息會傳回目前的 IME 模式偏差設定。</span><span class="sxs-lookup"><span data-stu-id="64d63-112">This message returns the current IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d63-113">備註</span><span class="sxs-lookup"><span data-stu-id="64d63-113">Remarks</span></span>

<span data-ttu-id="64d63-114">若要取得文字服務架構模式偏差，請使用 [**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)。</span><span class="sxs-lookup"><span data-stu-id="64d63-114">To get the Text Services Framework mode bias, use [**EM\_GETCTFMODEBIAS**](em-getctfmodebias.md).</span></span>

<span data-ttu-id="64d63-115">在呼叫此函式之前，應用程式應該呼叫 [**EM \_ ISIME**](em-isime.md) 。</span><span class="sxs-lookup"><span data-stu-id="64d63-115">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d63-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="64d63-116">Requirements</span></span>



| <span data-ttu-id="64d63-117">需求</span><span class="sxs-lookup"><span data-stu-id="64d63-117">Requirement</span></span> | <span data-ttu-id="64d63-118">值</span><span class="sxs-lookup"><span data-stu-id="64d63-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64d63-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64d63-119">Minimum supported client</span></span><br/> | <span data-ttu-id="64d63-120">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64d63-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64d63-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64d63-121">Minimum supported server</span></span><br/> | <span data-ttu-id="64d63-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64d63-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64d63-123">標頭</span><span class="sxs-lookup"><span data-stu-id="64d63-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d63-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="64d63-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d63-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64d63-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="64d63-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="64d63-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64d63-127">**EM \_ ISIME**</span><span class="sxs-lookup"><span data-stu-id="64d63-127">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="64d63-128">**EM \_ GETCTFMODEBIAS**</span><span class="sxs-lookup"><span data-stu-id="64d63-128">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> </dl>

 

 





