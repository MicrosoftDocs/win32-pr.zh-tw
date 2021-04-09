---
title: 'CDM_GETFOLDERIDLIST 訊息 (Commdlg .h) '
description: 抓取對應于目前開啟之 [Explorer 樣式開啟] 或 [另存新檔] 對話方塊之資料夾的專案識別碼清單位址。
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ac82a628d6fcace6863abb30e5703af02a948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686334"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="95e43-104">CDM \_ GETFOLDERIDLIST 訊息</span><span class="sxs-lookup"><span data-stu-id="95e43-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="95e43-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="95e43-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="95e43-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="95e43-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="95e43-107">抓取對應于目前開啟之 [Explorer 樣式 **開啟** ] 或 [ **另存** 新檔] 對話方塊之資料夾的專案識別碼清單位址。</span><span class="sxs-lookup"><span data-stu-id="95e43-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="95e43-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="95e43-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="95e43-109">參數</span><span class="sxs-lookup"><span data-stu-id="95e43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e43-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95e43-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95e43-111">*LParam* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95e43-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="95e43-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95e43-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95e43-113">接收專案識別碼清單的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="95e43-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e43-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="95e43-114">Return value</span></span>

<span data-ttu-id="95e43-115">如果訊息成功，則傳回值是專案識別碼清單的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="95e43-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="95e43-116">這是複製到緩衝區的位元組數目，如果緩衝區太小，則為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="95e43-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="95e43-117">如果發生錯誤，則傳回值小於零。</span><span class="sxs-lookup"><span data-stu-id="95e43-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e43-118">備註</span><span class="sxs-lookup"><span data-stu-id="95e43-118">Remarks</span></span>

<span data-ttu-id="95e43-119">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="95e43-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="95e43-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="95e43-120">Requirements</span></span>



| <span data-ttu-id="95e43-121">需求</span><span class="sxs-lookup"><span data-stu-id="95e43-121">Requirement</span></span> | <span data-ttu-id="95e43-122">值</span><span class="sxs-lookup"><span data-stu-id="95e43-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e43-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95e43-123">Minimum supported client</span></span><br/> | <span data-ttu-id="95e43-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95e43-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="95e43-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95e43-125">Minimum supported server</span></span><br/> | <span data-ttu-id="95e43-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95e43-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95e43-127">標頭</span><span class="sxs-lookup"><span data-stu-id="95e43-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e43-128"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="95e43-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e43-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95e43-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="95e43-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="95e43-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95e43-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="95e43-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="95e43-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="95e43-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="95e43-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="95e43-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="95e43-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="95e43-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="95e43-135">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="95e43-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

