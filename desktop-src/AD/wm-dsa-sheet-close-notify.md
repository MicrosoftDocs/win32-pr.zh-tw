---
title: WM_DSA_SHEET_CLOSE_NOTIFY 訊息
description: 當次要屬性工作表損毀時，張貼至 Active Directory MMC 嵌入式管理單元。
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- WM_DSA_SHEET_CLOSE_NOTIFY 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966118"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="dc555-104">WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知訊息</span><span class="sxs-lookup"><span data-stu-id="dc555-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="dc555-105">當次要屬性工作表損毀時，會將 **WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知** 訊息張貼至 Active Directory MMC 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="dc555-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="dc555-106">這個訊息值未定義于已發行的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="dc555-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="dc555-107">若要使用這個訊息值，您必須以所示的確切格式來定義它。</span><span class="sxs-lookup"><span data-stu-id="dc555-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="dc555-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc555-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc555-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="dc555-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="dc555-110">將處理此訊息之嵌入式管理單元視窗的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="dc555-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="dc555-111">這個控制碼是從 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **hwndHidden** 成員取得的。</span><span class="sxs-lookup"><span data-stu-id="dc555-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dc555-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc555-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc555-113">包含應用程式定義的32位值。</span><span class="sxs-lookup"><span data-stu-id="dc555-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="dc555-114">這是從 [**PROPSHEETCFG**](propsheetcfg.md)結構的 **wParamSheetClose** 成員取得的。</span><span class="sxs-lookup"><span data-stu-id="dc555-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dc555-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc555-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc555-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="dc555-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc555-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc555-117">Return value</span></span>

<span data-ttu-id="dc555-118">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="dc555-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc555-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc555-119">Requirements</span></span>



| <span data-ttu-id="dc555-120">需求</span><span class="sxs-lookup"><span data-stu-id="dc555-120">Requirement</span></span> | <span data-ttu-id="dc555-121">值</span><span class="sxs-lookup"><span data-stu-id="dc555-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dc555-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc555-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc555-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc555-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dc555-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc555-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc555-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc555-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc555-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc555-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc555-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="dc555-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





