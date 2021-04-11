---
title: 'MCIWNDM_OPEN 訊息 (Vfw .h) '
description: MCIWNDM \_ 開啟的訊息會開啟 MCI 裝置，並將其與 MCIWnd 視窗建立關聯。
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094384"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="848aa-104">MCIWNDM \_ 開啟的訊息</span><span class="sxs-lookup"><span data-stu-id="848aa-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="848aa-105">**MCIWNDM \_ 開啟** 的訊息會開啟 MCI 裝置，並將其與 MCIWnd 視窗建立關聯。</span><span class="sxs-lookup"><span data-stu-id="848aa-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="848aa-106">若為使用資料檔案的 MCI 裝置，此宏也可以開啟指定的資料檔案、為要建立的新檔案命名，或顯示對話方塊，讓使用者選取要開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="848aa-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="848aa-107">您可以使用 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="848aa-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="848aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="848aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="848aa-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="848aa-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="848aa-110">與要開啟的裝置或檔案相關聯的旗標。</span><span class="sxs-lookup"><span data-stu-id="848aa-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="848aa-111">MCIWNDOPENF \_ new 旗標會指定以 **szFile** 中指定的名稱建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="848aa-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="848aa-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span><span class="sxs-lookup"><span data-stu-id="848aa-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="848aa-113">以 null 結束的字串指標，識別要開啟的檔案名或 MCI 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="848aa-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="848aa-114">針對此參數指定1，以顯示 [開啟] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="848aa-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="848aa-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="848aa-115">Return Value</span></span>

<span data-ttu-id="848aa-116">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="848aa-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="848aa-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="848aa-117">Requirements</span></span>



| <span data-ttu-id="848aa-118">需求</span><span class="sxs-lookup"><span data-stu-id="848aa-118">Requirement</span></span> | <span data-ttu-id="848aa-119">值</span><span class="sxs-lookup"><span data-stu-id="848aa-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="848aa-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="848aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="848aa-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="848aa-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="848aa-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="848aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="848aa-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="848aa-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="848aa-124">標頭</span><span class="sxs-lookup"><span data-stu-id="848aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="848aa-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="848aa-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="848aa-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="848aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848aa-127">**MCIWndOpen**</span><span class="sxs-lookup"><span data-stu-id="848aa-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





