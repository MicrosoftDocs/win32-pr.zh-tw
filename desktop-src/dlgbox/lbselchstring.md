---
title: 'LBSELCHSTRING message (Commdlg) '
description: '[開啟] 或 [另存新檔] 對話方塊會在對話方塊的任何清單方塊或下拉式方塊中選取的專案變更時，將已註冊的 LBSELCHSTRING 訊息傳送至您的勾點程式。'
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- LBSELCHSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590765"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="79084-104">LBSELCHSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="79084-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="79084-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="79084-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="79084-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="79084-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="79084-107">[ **開啟** ] 或 [ **另存** 新檔] 對話方塊會在對話方塊的任何清單方塊或下拉式方塊中選取的專案變更時，將已註冊的 **LBSELCHSTRING** 訊息傳送至您的勾點程式。</span><span class="sxs-lookup"><span data-stu-id="79084-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="79084-108">參數</span><span class="sxs-lookup"><span data-stu-id="79084-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79084-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79084-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79084-110">選取範圍變更之清單方塊或下拉式方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="79084-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="79084-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79084-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79084-112">低序位字組會在清單方塊或下拉式方塊中指定選取之字串的專案編號。</span><span class="sxs-lookup"><span data-stu-id="79084-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="79084-113">高序位字組指定選取範圍變更的類型。</span><span class="sxs-lookup"><span data-stu-id="79084-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="79084-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="79084-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="79084-115">值</span><span class="sxs-lookup"><span data-stu-id="79084-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="79084-116">意義</span><span class="sxs-lookup"><span data-stu-id="79084-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="79084-117"><dt>**CD \_LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79084-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="79084-118">專案是單一選取清單方塊中唯一選取的專案。</span><span class="sxs-lookup"><span data-stu-id="79084-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="79084-119"><dt>**CD \_LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="79084-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="79084-120">專案是在多重選取清單方塊中選取的其中一個專案。</span><span class="sxs-lookup"><span data-stu-id="79084-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="79084-121"><dt>**CD \_LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="79084-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="79084-122">在多重選取清單方塊中，不會再選取該專案。</span><span class="sxs-lookup"><span data-stu-id="79084-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="79084-123"><dt>**CD \_LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="79084-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="79084-124">多重選取清單方塊中沒有任何專案存在。</span><span class="sxs-lookup"><span data-stu-id="79084-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79084-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="79084-125">Return value</span></span>

<span data-ttu-id="79084-126">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="79084-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79084-127">備註</span><span class="sxs-lookup"><span data-stu-id="79084-127">Remarks</span></span>

<span data-ttu-id="79084-128">攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **LBSELCHSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="79084-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="79084-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="79084-129">Requirements</span></span>



| <span data-ttu-id="79084-130">需求</span><span class="sxs-lookup"><span data-stu-id="79084-130">Requirement</span></span> | <span data-ttu-id="79084-131">值</span><span class="sxs-lookup"><span data-stu-id="79084-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79084-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79084-132">Minimum supported client</span></span><br/> | <span data-ttu-id="79084-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79084-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="79084-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79084-134">Minimum supported server</span></span><br/> | <span data-ttu-id="79084-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79084-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="79084-136">標頭</span><span class="sxs-lookup"><span data-stu-id="79084-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="79084-137"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="79084-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="79084-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="79084-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="79084-139">**LBSELCHSTRINGW** (Unicode) 和 **LBSELCHSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="79084-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="79084-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79084-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="79084-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="79084-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="79084-142">**CDN \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="79084-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="79084-143">**CDN \_ TYPECHANGE**</span><span class="sxs-lookup"><span data-stu-id="79084-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="79084-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="79084-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="79084-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="79084-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="79084-146">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="79084-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

