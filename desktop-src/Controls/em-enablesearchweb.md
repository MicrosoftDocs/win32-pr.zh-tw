---
title: 'EM_ENABLESEARCHWEB 訊息 (CommCtrl .h) '
description: 啟用或停用 [搜尋 web] 功能和內容功能表項目。
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_ENABLESEARCHWEB message Windows 控制項
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934634"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="747b0-104">EM \_ ENABLESEARCHWEB 訊息</span><span class="sxs-lookup"><span data-stu-id="747b0-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="747b0-105">啟用或停用 [搜尋 web] 功能和內容功能表項目。</span><span class="sxs-lookup"><span data-stu-id="747b0-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="747b0-106">參數</span><span class="sxs-lookup"><span data-stu-id="747b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="747b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="747b0-108">**TRUE** 值表示已啟用「搜尋 web」功能，而值為 **FALSE** 表示已停用。</span><span class="sxs-lookup"><span data-stu-id="747b0-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="747b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="747b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="747b0-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="747b0-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747b0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="747b0-111">Return value</span></span>

<span data-ttu-id="747b0-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="747b0-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="747b0-113">備註</span><span class="sxs-lookup"><span data-stu-id="747b0-113">Remarks</span></span>

<span data-ttu-id="747b0-114">如果您使用此訊息停用 [搜尋網路]， [**EM \_ SEARCHWEB**](em-searchweb.md) 訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="747b0-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="747b0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="747b0-115">Requirements</span></span>



| <span data-ttu-id="747b0-116">需求</span><span class="sxs-lookup"><span data-stu-id="747b0-116">Requirement</span></span> | <span data-ttu-id="747b0-117">值</span><span class="sxs-lookup"><span data-stu-id="747b0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="747b0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="747b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="747b0-119">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="747b0-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="747b0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="747b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="747b0-121">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="747b0-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="747b0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="747b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="747b0-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="747b0-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747b0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="747b0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="747b0-125">**參考**</span><span class="sxs-lookup"><span data-stu-id="747b0-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="747b0-126">**EM \_ SEARCHWEB**</span><span class="sxs-lookup"><span data-stu-id="747b0-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 





