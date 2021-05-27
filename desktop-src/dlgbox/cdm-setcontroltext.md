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
ms.openlocfilehash: 89c82a9144717224871caecf44da352a4e01cac2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550123"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="bf571-104">CDM \_ SETCONTROLTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="bf571-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="bf571-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bf571-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="bf571-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="bf571-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="bf571-107">在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中，設定指定之控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="bf571-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="bf571-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="bf571-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="bf571-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf571-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf571-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf571-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf571-111">要設定其文字之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf571-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="bf571-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf571-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf571-113">控制項的新文字。</span><span class="sxs-lookup"><span data-stu-id="bf571-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf571-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf571-114">Return value</span></span>

<span data-ttu-id="bf571-115">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bf571-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf571-116">備註</span><span class="sxs-lookup"><span data-stu-id="bf571-116">Remarks</span></span>

<span data-ttu-id="bf571-117">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="bf571-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="bf571-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf571-118">Requirements</span></span>



| <span data-ttu-id="bf571-119">需求</span><span class="sxs-lookup"><span data-stu-id="bf571-119">Requirement</span></span> | <span data-ttu-id="bf571-120">值</span><span class="sxs-lookup"><span data-stu-id="bf571-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf571-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf571-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bf571-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf571-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bf571-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf571-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bf571-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf571-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bf571-125">標頭</span><span class="sxs-lookup"><span data-stu-id="bf571-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf571-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bf571-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf571-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf571-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf571-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="bf571-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bf571-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="bf571-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="bf571-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="bf571-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="bf571-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="bf571-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="bf571-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="bf571-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bf571-133">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="bf571-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

