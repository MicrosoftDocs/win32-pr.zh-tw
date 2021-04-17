---
title: 'LB_ADDFILE 訊息 (Winuser .h) '
description: 將指定的檔案名加入包含目錄清單的清單方塊中。
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE message Windows 控制項
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466337"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="f2763-104">LB \_ ADDFILE 訊息</span><span class="sxs-lookup"><span data-stu-id="f2763-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="f2763-105">將指定的檔案名加入包含目錄清單的清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="f2763-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2763-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2763-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2763-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2763-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="f2763-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f2763-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2763-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2763-110">緩衝區的指標，指定要加入的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f2763-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2763-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2763-111">Return value</span></span>

<span data-ttu-id="f2763-112">傳回值是已加入之檔案的以零為起始的索引，如果發生錯誤，則為 LB \_ ERR。</span><span class="sxs-lookup"><span data-stu-id="f2763-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2763-113">備註</span><span class="sxs-lookup"><span data-stu-id="f2763-113">Remarks</span></span>

<span data-ttu-id="f2763-114">*LParam* 要加入的清單方塊必須已由 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)函數填滿。</span><span class="sxs-lookup"><span data-stu-id="f2763-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="f2763-115">[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="f2763-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="f2763-116">它會保留指定的記憶體數量，讓後續的 **LB \_ ADDFILE** 訊息能以最短的時間進行。</span><span class="sxs-lookup"><span data-stu-id="f2763-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="f2763-117">您可以使用 *wParam* 和 *lParam* 參數的估計值。</span><span class="sxs-lookup"><span data-stu-id="f2763-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="f2763-118">如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。</span><span class="sxs-lookup"><span data-stu-id="f2763-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="f2763-119">若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。</span><span class="sxs-lookup"><span data-stu-id="f2763-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="f2763-120">這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="f2763-120">This can cause problems.</span></span> <span data-ttu-id="f2763-121">例如，在日文視窗的非 Unicode 清單方塊中，重音的羅馬字元將會出現模糊。</span><span class="sxs-lookup"><span data-stu-id="f2763-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="f2763-122">若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。</span><span class="sxs-lookup"><span data-stu-id="f2763-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2763-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2763-123">Requirements</span></span>



| <span data-ttu-id="f2763-124">需求</span><span class="sxs-lookup"><span data-stu-id="f2763-124">Requirement</span></span> | <span data-ttu-id="f2763-125">值</span><span class="sxs-lookup"><span data-stu-id="f2763-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2763-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2763-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f2763-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2763-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f2763-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2763-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f2763-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2763-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2763-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f2763-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2763-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f2763-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2763-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2763-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2763-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="f2763-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f2763-134">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="f2763-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="f2763-135">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="f2763-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





