---
title: WM_DSA_SHEET_CREATE_NOTIFY 訊息
description: 張貼至 Active Directory MMC 嵌入式管理單元，以建立次要屬性工作表。
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CREATE_NOTIFY 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934454"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="b7e6b-104">WM \_ DSA \_ 工作表 \_ 建立 \_ 通知訊息</span><span class="sxs-lookup"><span data-stu-id="b7e6b-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="b7e6b-105">「 **WM \_ DSA \_ 工作表 \_ 建立 \_ 通知** 」訊息會張貼至 Active Directory MMC 嵌入式管理單元，以建立次要屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="b7e6b-106">這個訊息值未定義于已發行的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="b7e6b-107">若要使用這個訊息值，請以所示的確切格式來定義它。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="b7e6b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7e6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e6b-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="b7e6b-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e6b-110">將處理此訊息之嵌入式管理單元視窗的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="b7e6b-111">這個控制碼是從 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **hwndHidden** 成員取得的。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b7e6b-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7e6b-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e6b-113">包含 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md) 結構的指標，此結構會定義要建立的次要屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="b7e6b-114">當不再需要時，訊息接收器必須使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree) 函式釋放此記憶體。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="b7e6b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7e6b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e6b-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e6b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7e6b-117">Return value</span></span>

<span data-ttu-id="b7e6b-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="b7e6b-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e6b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7e6b-119">Requirements</span></span>



| <span data-ttu-id="b7e6b-120">需求</span><span class="sxs-lookup"><span data-stu-id="b7e6b-120">Requirement</span></span> | <span data-ttu-id="b7e6b-121">值</span><span class="sxs-lookup"><span data-stu-id="b7e6b-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b7e6b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7e6b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e6b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7e6b-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b7e6b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7e6b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e6b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7e6b-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7e6b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7e6b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e6b-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="b7e6b-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="b7e6b-128">**DSA \_ 秒 \_ 頁面 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b7e6b-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="b7e6b-129">**>localfree**</span><span class="sxs-lookup"><span data-stu-id="b7e6b-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

