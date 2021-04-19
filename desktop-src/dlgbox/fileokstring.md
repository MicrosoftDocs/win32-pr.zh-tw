---
title: 'FILEOKSTRING message (Commdlg) '
description: 當使用者指定檔案名，然後按一下 [確定] 按鈕時，[開啟] 或 [另存新檔] 對話方塊會將已註冊的 FILEOKSTRING 訊息傳送至您的攔截程式 OFNHookProc。
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- FILEOKSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6fddbb3460f15e1efb946b9bd17f1c85fd031a8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590785"
---
# <a name="fileokstring-message"></a><span data-ttu-id="68755-104">FILEOKSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="68755-104">FILEOKSTRING message</span></span>

<span data-ttu-id="68755-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="68755-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="68755-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="68755-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="68755-107">當使用者指定檔案名，然後按一下 [**確定]** 按鈕時，[**開啟**] 或 [**另存** 新檔] 對話方塊會將已註冊的 **FILEOKSTRING** 訊息傳送至您的攔截程式 [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)。</span><span class="sxs-lookup"><span data-stu-id="68755-107">An **Open** or **Save As** dialog box sends the **FILEOKSTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), when the user specifies a file name and clicks the **OK** button.</span></span> <span data-ttu-id="68755-108">攔截程式可以接受檔案名，並允許對話方塊關閉或拒絕檔案名，並強制對話方塊維持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="68755-108">The hook procedure can accept the file name and allow the dialog box to close, or reject the file name and force the dialog box to remain open.</span></span>


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a><span data-ttu-id="68755-109">參數</span><span class="sxs-lookup"><span data-stu-id="68755-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68755-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68755-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68755-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="68755-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="68755-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68755-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68755-113">[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="68755-113">A pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="68755-114">此結構的 **lpstrFile** 成員包含使用者所指定的磁片磁碟機、路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="68755-114">The **lpstrFile** member of this structure contains the drive, path, and file name specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68755-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="68755-115">Return value</span></span>

<span data-ttu-id="68755-116">如果攔截程式傳回零，則 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊會接受指定的檔案名並關閉。</span><span class="sxs-lookup"><span data-stu-id="68755-116">If the hook procedure returns zero, the **Open** or **Save As** dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="68755-117">如果攔截程式傳回非零值，[ **開啟** ] 或 [ **另存** 新檔] 對話方塊會拒絕指定的檔案名並保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="68755-117">If the hook procedure returns a nonzero value, the **Open** or **Save As** dialog box rejects the specified file name and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="68755-118">備註</span><span class="sxs-lookup"><span data-stu-id="68755-118">Remarks</span></span>

<span data-ttu-id="68755-119">攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **FILEOKSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="68755-119">The hook procedure must specify the **FILEOKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="68755-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="68755-120">Requirements</span></span>



| <span data-ttu-id="68755-121">需求</span><span class="sxs-lookup"><span data-stu-id="68755-121">Requirement</span></span> | <span data-ttu-id="68755-122">值</span><span class="sxs-lookup"><span data-stu-id="68755-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68755-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68755-123">Minimum supported client</span></span><br/> | <span data-ttu-id="68755-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68755-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="68755-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68755-125">Minimum supported server</span></span><br/> | <span data-ttu-id="68755-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68755-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="68755-127">標頭</span><span class="sxs-lookup"><span data-stu-id="68755-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68755-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="68755-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="68755-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="68755-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="68755-130">**FILEOKSTRINGW** (Unicode) 和 **FILEOKSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="68755-130">**FILEOKSTRINGW** (Unicode) and **FILEOKSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="68755-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68755-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="68755-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="68755-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68755-133">**CDN \_ FILEOK**</span><span class="sxs-lookup"><span data-stu-id="68755-133">**CDN\_FILEOK**</span></span>](cdn-fileok.md)
</dt> <dt>

[<span data-ttu-id="68755-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="68755-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="68755-135">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="68755-135">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="68755-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="68755-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68755-137">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="68755-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

