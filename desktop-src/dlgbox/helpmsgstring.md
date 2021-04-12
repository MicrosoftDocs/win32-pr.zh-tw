---
title: 'HELPMSGSTRING message (Commdlg) '
description: 當使用者按一下 [說明] 按鈕時，通用的對話方塊會將已註冊的 HELPMSGSTRING 訊息傳送至其擁有者視窗的視窗程式。
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- HELPMSGSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106013"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="39b29-104">HELPMSGSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="39b29-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="39b29-105">當使用者按一下 [說明 **] 按鈕時**，通用的對話方塊會將已註冊的 **HELPMSGSTRING** 訊息傳送至其擁有者視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="39b29-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="39b29-106">參數</span><span class="sxs-lookup"><span data-stu-id="39b29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39b29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39b29-108">通用對話方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="39b29-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="39b29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39b29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39b29-110">通用對話方塊之初始化結構的指標。</span><span class="sxs-lookup"><span data-stu-id="39b29-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="39b29-111">此結構可以是 [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)、 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)、 [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)、 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)、 [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) 或 [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) 結構。</span><span class="sxs-lookup"><span data-stu-id="39b29-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b29-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="39b29-112">Return value</span></span>

<span data-ttu-id="39b29-113">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="39b29-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b29-114">備註</span><span class="sxs-lookup"><span data-stu-id="39b29-114">Remarks</span></span>

<span data-ttu-id="39b29-115">您必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **HELPMSGSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39b29-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="39b29-116">當您建立對話方塊時，請使用初始化結構的 **hwndOwner** 成員來識別要接收 **HELPMSGSTRING** 訊息的視窗。</span><span class="sxs-lookup"><span data-stu-id="39b29-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b29-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="39b29-117">Requirements</span></span>



| <span data-ttu-id="39b29-118">需求</span><span class="sxs-lookup"><span data-stu-id="39b29-118">Requirement</span></span> | <span data-ttu-id="39b29-119">值</span><span class="sxs-lookup"><span data-stu-id="39b29-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b29-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39b29-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39b29-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39b29-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39b29-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39b29-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39b29-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39b29-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39b29-124">標頭</span><span class="sxs-lookup"><span data-stu-id="39b29-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b29-125"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="39b29-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="39b29-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="39b29-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39b29-127">**HELPMSGSTRINGW** (Unicode) 和 **HELPMSGSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="39b29-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="39b29-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39b29-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="39b29-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="39b29-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39b29-130">**CDN \_ 說明**</span><span class="sxs-lookup"><span data-stu-id="39b29-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="39b29-131">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="39b29-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="39b29-132">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="39b29-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="39b29-133">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="39b29-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="39b29-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="39b29-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="39b29-135">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="39b29-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="39b29-136">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="39b29-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="39b29-137">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="39b29-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="39b29-138">**概念**</span><span class="sxs-lookup"><span data-stu-id="39b29-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="39b29-139">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="39b29-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

