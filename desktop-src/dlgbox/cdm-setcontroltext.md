---
title: 'CDM_SETCONTROLTEXT 訊息 (Commdlg .h) '
description: 在 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊中，設定指定之控制項的文字。
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- CDM_SETCONTROLTEXT 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87490ba20b5785da4fb9660d97b1b9232d047671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383802"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="78f1c-104">CDM \_ SETCONTROLTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="78f1c-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="78f1c-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="78f1c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="78f1c-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="78f1c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="78f1c-107">在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中，設定指定之控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="78f1c-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="78f1c-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="78f1c-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="78f1c-109">參數</span><span class="sxs-lookup"><span data-stu-id="78f1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f1c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78f1c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78f1c-111">要設定其文字之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78f1c-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="78f1c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78f1c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78f1c-113">控制項的新文字。</span><span class="sxs-lookup"><span data-stu-id="78f1c-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f1c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="78f1c-114">Return value</span></span>

<span data-ttu-id="78f1c-115">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="78f1c-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78f1c-116">備註</span><span class="sxs-lookup"><span data-stu-id="78f1c-116">Remarks</span></span>

<span data-ttu-id="78f1c-117">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="78f1c-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="78f1c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="78f1c-118">Requirements</span></span>



| <span data-ttu-id="78f1c-119">需求</span><span class="sxs-lookup"><span data-stu-id="78f1c-119">Requirement</span></span> | <span data-ttu-id="78f1c-120">值</span><span class="sxs-lookup"><span data-stu-id="78f1c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f1c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78f1c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="78f1c-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78f1c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="78f1c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78f1c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="78f1c-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78f1c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78f1c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="78f1c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="78f1c-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="78f1c-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f1c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78f1c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="78f1c-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="78f1c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78f1c-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="78f1c-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="78f1c-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="78f1c-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="78f1c-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="78f1c-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="78f1c-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="78f1c-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="78f1c-133">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="78f1c-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

