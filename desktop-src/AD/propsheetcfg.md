---
title: PROPSHEETCFG 結構
description: 用來包含屬性工作表設定資料。
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- PROPSHEETCFG 結構 Active Directory
- PPROPSHEETCFG 結構指標 Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025132"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="4d6b0-105">PROPSHEETCFG 結構</span><span class="sxs-lookup"><span data-stu-id="4d6b0-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="4d6b0-106">**PROPSHEETCFG** 結構是用來包含屬性工作表設定資料。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="4d6b0-107">此結構包含在 [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) 剪貼簿格式中。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="4d6b0-108">此結構未定義于已發行的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="4d6b0-109">若要使用這個結構，您必須以所示的確切格式來定義它。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4d6b0-110">語法</span><span class="sxs-lookup"><span data-stu-id="4d6b0-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="4d6b0-111">成員</span><span class="sxs-lookup"><span data-stu-id="4d6b0-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d6b0-112">**lNotifyHandle**</span><span class="sxs-lookup"><span data-stu-id="4d6b0-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4d6b0-113">包含通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-113">Contains the notification handle.</span></span> <span data-ttu-id="4d6b0-114">這與針對 [**IExtendPropertySheet2：： CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85))方法中的 *控制碼* 參數傳遞的控制碼相同。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="4d6b0-115">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="4d6b0-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="4d6b0-116">包含父屬性工作表的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="4d6b0-117">**hwndHidden**</span><span class="sxs-lookup"><span data-stu-id="4d6b0-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="4d6b0-118">包含隱藏視窗的控點。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="4d6b0-119">**wParamSheetClose**</span><span class="sxs-lookup"><span data-stu-id="4d6b0-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="4d6b0-120">包含應用程式定義的32位值。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="4d6b0-121">此值會在「 [**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)」訊息的 *wParam* 中傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="4d6b0-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d6b0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d6b0-122">Requirements</span></span>



| <span data-ttu-id="4d6b0-123">需求</span><span class="sxs-lookup"><span data-stu-id="4d6b0-123">Requirement</span></span> | <span data-ttu-id="4d6b0-124">值</span><span class="sxs-lookup"><span data-stu-id="4d6b0-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4d6b0-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d6b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4d6b0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d6b0-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4d6b0-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d6b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4d6b0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d6b0-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d6b0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d6b0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d6b0-130">**CFSTR \_ DS \_ PROPSHEETCONFIG**</span><span class="sxs-lookup"><span data-stu-id="4d6b0-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="4d6b0-131">**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="4d6b0-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

