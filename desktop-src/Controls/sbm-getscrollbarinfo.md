---
title: 'SBM_GETSCROLLBARINFO 訊息 (Winuser .h) '
description: 由應用程式傳送以取得指定捲軸的相關資訊。
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- SBM_GETSCROLLBARINFO message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685876"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="56362-104">SBM \_ GETSCROLLBARINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="56362-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="56362-105">由應用程式傳送以取得指定捲軸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56362-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="56362-106">參數</span><span class="sxs-lookup"><span data-stu-id="56362-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56362-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56362-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56362-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="56362-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56362-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56362-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56362-110">接收資訊之 [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="56362-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56362-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="56362-111">Return value</span></span>

<span data-ttu-id="56362-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="56362-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="56362-113">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="56362-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="56362-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="56362-114">Requirements</span></span>



| <span data-ttu-id="56362-115">需求</span><span class="sxs-lookup"><span data-stu-id="56362-115">Requirement</span></span> | <span data-ttu-id="56362-116">值</span><span class="sxs-lookup"><span data-stu-id="56362-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56362-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56362-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56362-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56362-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56362-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56362-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56362-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56362-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="56362-121">標頭</span><span class="sxs-lookup"><span data-stu-id="56362-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="56362-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="56362-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56362-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56362-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="56362-124">**參考**</span><span class="sxs-lookup"><span data-stu-id="56362-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="56362-125">**GetScrollBarInfo**</span><span class="sxs-lookup"><span data-stu-id="56362-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="56362-126">**SCROLLBARINFO**</span><span class="sxs-lookup"><span data-stu-id="56362-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

