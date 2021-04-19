---
title: 'CDM_GETSPEC 訊息 (Commdlg .h) '
description: 抓取檔案名 (不包含在 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊中目前選取之檔案的路徑) 。
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- CDM_GETSPEC 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938536ea7cc72ebb950420ad3d5c9bd35c64db72
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590925"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="ebd69-104">CDM \_ GETSPEC 訊息</span><span class="sxs-lookup"><span data-stu-id="ebd69-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="ebd69-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ebd69-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="ebd69-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="ebd69-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ebd69-107">抓取檔案名 (不包含在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中目前選取之檔案的路徑) 。</span><span class="sxs-lookup"><span data-stu-id="ebd69-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="ebd69-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="ebd69-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="ebd69-109">參數</span><span class="sxs-lookup"><span data-stu-id="ebd69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd69-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebd69-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebd69-111">*LParam* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="ebd69-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ebd69-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebd69-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebd69-113">接收檔案名之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="ebd69-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd69-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebd69-114">Return value</span></span>

<span data-ttu-id="ebd69-115">如果訊息成功，傳回值就是檔案名字串的大小（以字元為單位），包括結束的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="ebd69-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="ebd69-116">這是複製到緩衝區的位元組數或字元數，如果緩衝區太小，則為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="ebd69-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="ebd69-117">如果發生錯誤，則傳回值小於零。</span><span class="sxs-lookup"><span data-stu-id="ebd69-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd69-118">備註</span><span class="sxs-lookup"><span data-stu-id="ebd69-118">Remarks</span></span>

<span data-ttu-id="ebd69-119">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="ebd69-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="ebd69-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebd69-120">Requirements</span></span>



| <span data-ttu-id="ebd69-121">需求</span><span class="sxs-lookup"><span data-stu-id="ebd69-121">Requirement</span></span> | <span data-ttu-id="ebd69-122">值</span><span class="sxs-lookup"><span data-stu-id="ebd69-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd69-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebd69-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd69-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebd69-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ebd69-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebd69-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd69-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebd69-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebd69-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ebd69-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd69-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ebd69-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd69-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebd69-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebd69-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="ebd69-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ebd69-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ebd69-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ebd69-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ebd69-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ebd69-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="ebd69-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="ebd69-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="ebd69-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ebd69-135">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="ebd69-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

