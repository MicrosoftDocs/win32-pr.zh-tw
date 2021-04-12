---
title: 'COLOROKSTRING message (Commdlg) '
description: 當使用者選取色彩，然後按一下 [確定] 按鈕時，[色彩] 對話方塊會將已註冊的 COLOROKSTRING 訊息傳送至您的掛勾程式 CCHookProc。
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- COLOROKSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103649"
---
# <a name="colorokstring-message"></a><span data-ttu-id="5f281-104">COLOROKSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="5f281-104">COLOROKSTRING message</span></span>

<span data-ttu-id="5f281-105">當使用者選取色彩，然後按一下 [**確定]** 按鈕時，[**色彩**] 對話方塊會將已註冊的 **COLOROKSTRING** 訊息傳送至您的掛勾程式 [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)。</span><span class="sxs-lookup"><span data-stu-id="5f281-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="5f281-106">攔截程式可以接受色彩，並允許對話方塊關閉或拒絕色彩，然後強制對話方塊保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="5f281-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="5f281-107">參數</span><span class="sxs-lookup"><span data-stu-id="5f281-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f281-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f281-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f281-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="5f281-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5f281-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f281-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f281-111">[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5f281-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="5f281-112">此結構的 **rgbResult** 成員包含所選色彩的 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="5f281-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f281-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f281-113">Return value</span></span>

<span data-ttu-id="5f281-114">如果攔截程式傳回零，[ **色彩** ] 對話方塊會接受選取的色彩並關閉。</span><span class="sxs-lookup"><span data-stu-id="5f281-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="5f281-115">如果攔截程式傳回非零值，[ **色彩** ] 對話方塊會拒絕選取的色彩並保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="5f281-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f281-116">備註</span><span class="sxs-lookup"><span data-stu-id="5f281-116">Remarks</span></span>

<span data-ttu-id="5f281-117">攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **COLOROKSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f281-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f281-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f281-118">Requirements</span></span>



| <span data-ttu-id="5f281-119">需求</span><span class="sxs-lookup"><span data-stu-id="5f281-119">Requirement</span></span> | <span data-ttu-id="5f281-120">值</span><span class="sxs-lookup"><span data-stu-id="5f281-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f281-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f281-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f281-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f281-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5f281-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f281-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f281-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f281-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f281-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5f281-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f281-126"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5f281-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5f281-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="5f281-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5f281-128">**COLOROKSTRINGW** (Unicode) 和 **COLOROKSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="5f281-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="5f281-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f281-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f281-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="5f281-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f281-131">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="5f281-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="5f281-132">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="5f281-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="5f281-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="5f281-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f281-134">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="5f281-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

