---
title: 'CDM_GETFOLDERPATH 訊息 (Commdlg .h) '
description: 抓取 Explorer 樣式 [開啟] 或 [另存新檔] 對話方塊中目前開啟之資料夾或目錄的路徑。
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590935"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="5c497-104">CDM \_ GETFOLDERPATH 訊息</span><span class="sxs-lookup"><span data-stu-id="5c497-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="5c497-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5c497-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="5c497-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="5c497-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5c497-107">抓取 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中目前開啟之資料夾或目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="5c497-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="5c497-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="5c497-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="5c497-109">參數</span><span class="sxs-lookup"><span data-stu-id="5c497-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c497-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c497-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c497-111">*LParam* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c497-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5c497-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c497-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c497-113">接收路徑之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="5c497-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c497-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c497-114">Return value</span></span>

<span data-ttu-id="5c497-115">如果訊息成功，傳回值就是路徑字串的大小（以字元為單位），包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="5c497-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="5c497-116">這是複製到緩衝區的位元組數或字元數，如果緩衝區太小，則為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="5c497-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="5c497-117">如果發生錯誤，則傳回值小於零。</span><span class="sxs-lookup"><span data-stu-id="5c497-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c497-118">備註</span><span class="sxs-lookup"><span data-stu-id="5c497-118">Remarks</span></span>

<span data-ttu-id="5c497-119">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="5c497-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="5c497-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c497-120">Requirements</span></span>



| <span data-ttu-id="5c497-121">需求</span><span class="sxs-lookup"><span data-stu-id="5c497-121">Requirement</span></span> | <span data-ttu-id="5c497-122">值</span><span class="sxs-lookup"><span data-stu-id="5c497-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c497-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c497-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5c497-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c497-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5c497-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c497-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5c497-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c497-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5c497-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5c497-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c497-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5c497-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c497-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c497-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c497-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="5c497-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c497-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="5c497-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="5c497-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5c497-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="5c497-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="5c497-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="5c497-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="5c497-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c497-135">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="5c497-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

