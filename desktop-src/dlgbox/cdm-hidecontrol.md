---
title: 'CDM_HIDECONTROL 訊息 (Commdlg .h) '
description: 在 Explorer 樣式的 [開啟] 或 [另存新檔] 對話方塊中隱藏指定的控制項。
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- CDM_HIDECONTROL 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f1a5a7a1830ceeb2c3671b0dfb538ad89e0a58
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548653"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="fea83-104">CDM \_ HIDECONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="fea83-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="fea83-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="fea83-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="fea83-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="fea83-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="fea83-107">在 Explorer 樣式的 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中隱藏指定的控制項。</span><span class="sxs-lookup"><span data-stu-id="fea83-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="fea83-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="fea83-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="fea83-109">參數</span><span class="sxs-lookup"><span data-stu-id="fea83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea83-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fea83-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea83-111">要隱藏之控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fea83-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="fea83-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fea83-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fea83-113">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="fea83-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea83-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fea83-114">Return value</span></span>

<span data-ttu-id="fea83-115">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="fea83-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fea83-116">備註</span><span class="sxs-lookup"><span data-stu-id="fea83-116">Remarks</span></span>

<span data-ttu-id="fea83-117">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="fea83-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="fea83-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fea83-118">Requirements</span></span>



| <span data-ttu-id="fea83-119">需求</span><span class="sxs-lookup"><span data-stu-id="fea83-119">Requirement</span></span> | <span data-ttu-id="fea83-120">值</span><span class="sxs-lookup"><span data-stu-id="fea83-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fea83-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fea83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fea83-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fea83-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fea83-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fea83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fea83-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fea83-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fea83-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fea83-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea83-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fea83-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea83-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fea83-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="fea83-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="fea83-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fea83-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="fea83-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="fea83-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="fea83-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="fea83-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="fea83-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="fea83-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="fea83-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fea83-133">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="fea83-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

