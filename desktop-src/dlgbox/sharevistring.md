---
title: 'SHAREVISTRING message (Commdlg) '
description: '[開啟] 或 [另存新檔] 對話方塊會將已註冊的 SHAREVISTRING 訊息傳送至您的攔截程式 OFNHookProc，如果當使用者按一下 [確定] 按鈕時，所選取的檔案發生共用違規。'
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- SHAREVISTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466149"
---
# <a name="sharevistring-message"></a><span data-ttu-id="5934e-104">SHAREVISTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="5934e-104">SHAREVISTRING message</span></span>

<span data-ttu-id="5934e-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5934e-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="5934e-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="5934e-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5934e-107">[ **開啟** ] 或 [ **另存** 新檔] 對話方塊會將已註冊的 **SHAREVISTRING** 訊息傳送至您的攔截程式 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)，如果當使用者按一下 [ **確定]** 按鈕時，所選取的檔案發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="5934e-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="5934e-108">參數</span><span class="sxs-lookup"><span data-stu-id="5934e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5934e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5934e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5934e-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="5934e-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5934e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5934e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5934e-112">[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5934e-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="5934e-113">此結構的 **lpstrFile** 成員包含造成共用違規的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5934e-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5934e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5934e-114">Return value</span></span>

<span data-ttu-id="5934e-115">攔截程式必須傳回下列其中一個值，以指出對話方塊應該如何處理共用違規。</span><span class="sxs-lookup"><span data-stu-id="5934e-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="5934e-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5934e-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="5934e-117">Description</span><span class="sxs-lookup"><span data-stu-id="5934e-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5934e-118"><dt>**OFN \_SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5934e-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="5934e-119">接受檔案名</span><span class="sxs-lookup"><span data-stu-id="5934e-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="5934e-120"><dt>**OFN \_SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5934e-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="5934e-121">拒絕檔案名，但不警告使用者。</span><span class="sxs-lookup"><span data-stu-id="5934e-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="5934e-122">應用程式會負責顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="5934e-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="5934e-123"><dt>**OFN \_SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5934e-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="5934e-124">拒絕檔案名，並顯示一則警告訊息， (與沒有攔截程式) 的結果相同。</span><span class="sxs-lookup"><span data-stu-id="5934e-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="5934e-125">備註</span><span class="sxs-lookup"><span data-stu-id="5934e-125">Remarks</span></span>

<span data-ttu-id="5934e-126">攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **SHAREVISTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5934e-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="5934e-127">只有當您在建立對話方塊時未在 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的 **旗標** 成員中指定 **OFN \_ SHAREAWARE** 旗標時，對話方塊才會傳送 **SHAREVISTRING** 註冊的訊息。</span><span class="sxs-lookup"><span data-stu-id="5934e-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="5934e-128">如果攔截程式傳回未定義的值，對話方塊會以 **OFN \_ SHAREWARN** 的方式回應。</span><span class="sxs-lookup"><span data-stu-id="5934e-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="5934e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5934e-129">Requirements</span></span>



| <span data-ttu-id="5934e-130">需求</span><span class="sxs-lookup"><span data-stu-id="5934e-130">Requirement</span></span> | <span data-ttu-id="5934e-131">值</span><span class="sxs-lookup"><span data-stu-id="5934e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5934e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5934e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5934e-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5934e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5934e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5934e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5934e-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5934e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5934e-136">標頭</span><span class="sxs-lookup"><span data-stu-id="5934e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5934e-137"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5934e-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5934e-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5934e-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5934e-139">**SHAREVISTRINGW** (Unicode) 和 **SHAREVISTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5934e-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="5934e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5934e-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="5934e-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="5934e-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5934e-142">**CDN \_ SHAREVIOLATION**</span><span class="sxs-lookup"><span data-stu-id="5934e-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="5934e-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="5934e-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="5934e-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="5934e-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="5934e-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="5934e-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5934e-146">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="5934e-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

