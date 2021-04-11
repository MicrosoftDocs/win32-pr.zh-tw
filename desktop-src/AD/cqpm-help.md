---
title: 'CQPM_HELP 訊息 (Cmnquery .h) '
description: 傳送至查詢表單延伸頁面的 CQPageProc 回呼函式，以允許頁面擴充功能顯示網頁的即時線上說明。
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- CQPM_HELP 訊息 Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094015"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="9b90c-104">CQPM 說明 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="9b90c-104">CQPM\_HELP message</span></span>

<span data-ttu-id="9b90c-105">**CQPM 說明 \_** 訊息會傳送至查詢表單延伸頁面的 [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)回呼函式，以允許頁面擴充功能顯示網頁的即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="9b90c-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="9b90c-106">可能的話，查詢頁面擴充功能應該會顯示即時線上說明以回應此事件。</span><span class="sxs-lookup"><span data-stu-id="9b90c-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b90c-107">參數</span><span class="sxs-lookup"><span data-stu-id="9b90c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b90c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b90c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b90c-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="9b90c-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9b90c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b90c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b90c-111">[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的指標，其中包含有關功能表項目、控制項、對話方塊或視窗的其他資料，而這些資料會要求內容相關的協助。</span><span class="sxs-lookup"><span data-stu-id="9b90c-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b90c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b90c-112">Return value</span></span>

<span data-ttu-id="9b90c-113">此訊息的傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="9b90c-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b90c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b90c-114">Requirements</span></span>



| <span data-ttu-id="9b90c-115">需求</span><span class="sxs-lookup"><span data-stu-id="9b90c-115">Requirement</span></span> | <span data-ttu-id="9b90c-116">值</span><span class="sxs-lookup"><span data-stu-id="9b90c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b90c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b90c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9b90c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b90c-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="9b90c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b90c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9b90c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b90c-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="9b90c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9b90c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b90c-122"><dt>Cmnquery。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b90c-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b90c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b90c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b90c-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="9b90c-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="9b90c-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="9b90c-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

