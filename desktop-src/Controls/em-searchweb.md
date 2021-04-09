---
title: 'EM_SEARCHWEB 訊息 (Commctrl .h) '
description: 開啟瀏覽器，並使用選取的文字做為搜尋字詞來執行 web 搜尋。
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844043"
---
# <a name="em_searchweb-message"></a><span data-ttu-id="50fbf-104">EM \_ SEARCHWEB 訊息</span><span class="sxs-lookup"><span data-stu-id="50fbf-104">EM\_SEARCHWEB message</span></span>

<span data-ttu-id="50fbf-105">開啟瀏覽器，並使用選取的文字做為搜尋字詞來執行 web 搜尋。</span><span class="sxs-lookup"><span data-stu-id="50fbf-105">Opens the browser and performs a web search with the selected text as the search term.</span></span>

## <a name="parameters"></a><span data-ttu-id="50fbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="50fbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50fbf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50fbf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50fbf-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="50fbf-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50fbf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50fbf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50fbf-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="50fbf-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50fbf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="50fbf-111">Return value</span></span>

<span data-ttu-id="50fbf-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="50fbf-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50fbf-113">備註</span><span class="sxs-lookup"><span data-stu-id="50fbf-113">Remarks</span></span>

<span data-ttu-id="50fbf-114">如果使用 [**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md) 訊息停用「搜尋 web」功能，則此訊息不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="50fbf-114">If the "Search the web" feature is disabled using the [**EM\_ENABLESEARCHWEB**](em-enablesearchweb.md) message, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="50fbf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="50fbf-115">Requirements</span></span>



| <span data-ttu-id="50fbf-116">需求</span><span class="sxs-lookup"><span data-stu-id="50fbf-116">Requirement</span></span> | <span data-ttu-id="50fbf-117">值</span><span class="sxs-lookup"><span data-stu-id="50fbf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50fbf-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50fbf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50fbf-119">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50fbf-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50fbf-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50fbf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50fbf-121">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50fbf-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50fbf-122">標頭</span><span class="sxs-lookup"><span data-stu-id="50fbf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="50fbf-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="50fbf-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50fbf-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50fbf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fbf-125">**EM \_ ENABLESEARCHWEB**</span><span class="sxs-lookup"><span data-stu-id="50fbf-125">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> </dl>

 

 





