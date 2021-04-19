---
title: 'CDM_GETFILEPATH 訊息 (Commdlg .h) '
description: 在 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊中，抓取所選取檔案的路徑和檔案名。
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdb7739cd2ab66362e18cc70f9937e75f80a82d9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590915"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="34468-104">CDM \_ GETFILEPATH 訊息</span><span class="sxs-lookup"><span data-stu-id="34468-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="34468-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34468-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="34468-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="34468-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="34468-107">在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中，抓取所選取檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="34468-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="34468-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="34468-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="34468-109">參數</span><span class="sxs-lookup"><span data-stu-id="34468-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34468-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34468-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34468-111">*LParam* 緩衝區的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="34468-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="34468-112">針對 ANSI 版本，這是位元組數;若為 Unicode 版本，這就是字元數目。</span><span class="sxs-lookup"><span data-stu-id="34468-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="34468-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34468-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34468-114">接收檔案名和路徑之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="34468-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34468-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="34468-115">Return value</span></span>

<span data-ttu-id="34468-116">如果訊息成功，則傳回值是檔案名和路徑字串的大小（以字元為單位），包括結束的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="34468-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="34468-117">這是複製到緩衝區的位元組數或字元數，如果緩衝區太小，則為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="34468-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="34468-118">如果發生錯誤，則傳回值小於零。</span><span class="sxs-lookup"><span data-stu-id="34468-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="34468-119">備註</span><span class="sxs-lookup"><span data-stu-id="34468-119">Remarks</span></span>

<span data-ttu-id="34468-120">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="34468-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="34468-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="34468-121">Requirements</span></span>



| <span data-ttu-id="34468-122">需求</span><span class="sxs-lookup"><span data-stu-id="34468-122">Requirement</span></span> | <span data-ttu-id="34468-123">值</span><span class="sxs-lookup"><span data-stu-id="34468-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34468-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34468-124">Minimum supported client</span></span><br/> | <span data-ttu-id="34468-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34468-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="34468-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34468-126">Minimum supported server</span></span><br/> | <span data-ttu-id="34468-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34468-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34468-128">標頭</span><span class="sxs-lookup"><span data-stu-id="34468-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="34468-129"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="34468-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34468-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34468-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="34468-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="34468-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="34468-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="34468-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="34468-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="34468-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="34468-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="34468-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="34468-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="34468-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="34468-136">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="34468-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

