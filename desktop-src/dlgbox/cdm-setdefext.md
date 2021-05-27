---
title: 'CDM_SETDEFEXT 訊息 (Commdlg .h) '
description: 設定 Explorer 樣式 [開啟] 或 [另存新檔] 對話方塊的預設副檔名。
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- CDM_SETDEFEXT 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b1169a2777d5a5f82925366c6723af741706d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550113"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="53079-104">CDM \_ SETDEFEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="53079-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="53079-105">\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="53079-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="53079-106">我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]</span><span class="sxs-lookup"><span data-stu-id="53079-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="53079-107">設定 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊的預設副檔名。</span><span class="sxs-lookup"><span data-stu-id="53079-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="53079-108">您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="53079-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="53079-109">參數</span><span class="sxs-lookup"><span data-stu-id="53079-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53079-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53079-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53079-111">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="53079-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="53079-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53079-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53079-113">新的副檔名指標。</span><span class="sxs-lookup"><span data-stu-id="53079-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="53079-114">不得包含點 (。 ) 。</span><span class="sxs-lookup"><span data-stu-id="53079-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53079-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="53079-115">Return value</span></span>

<span data-ttu-id="53079-116">此訊息沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="53079-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53079-117">備註</span><span class="sxs-lookup"><span data-stu-id="53079-117">Remarks</span></span>

<span data-ttu-id="53079-118">對應的宏如下所示：</span><span class="sxs-lookup"><span data-stu-id="53079-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="53079-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="53079-119">Requirements</span></span>



| <span data-ttu-id="53079-120">需求</span><span class="sxs-lookup"><span data-stu-id="53079-120">Requirement</span></span> | <span data-ttu-id="53079-121">值</span><span class="sxs-lookup"><span data-stu-id="53079-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53079-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53079-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53079-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53079-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="53079-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53079-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53079-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53079-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53079-126">標頭</span><span class="sxs-lookup"><span data-stu-id="53079-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="53079-127"><dt>Commdlg (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="53079-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53079-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53079-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="53079-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="53079-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53079-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="53079-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="53079-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="53079-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="53079-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="53079-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="53079-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="53079-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53079-134">通用對話方塊程式庫</span><span class="sxs-lookup"><span data-stu-id="53079-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

