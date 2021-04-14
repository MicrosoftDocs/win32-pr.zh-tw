---
title: 'MCIWNDM_OPENINTERFACE 訊息 (Vfw .h) '
description: MCIWNDM \_ OPENINTERFACE 訊息會將與指定介面相關聯的資料流程或檔案附加至 MCIWnd 視窗。 您可以使用 MCIWndOpenInterface 宏明確地傳送此訊息。
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383849"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="bc181-105">MCIWNDM \_ OPENINTERFACE 訊息</span><span class="sxs-lookup"><span data-stu-id="bc181-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="bc181-106">**MCIWNDM \_ OPENINTERFACE** 訊息會將與指定介面相關聯的資料流程或檔案附加至 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="bc181-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="bc181-107">您可以使用 [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="bc181-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="bc181-108">參數</span><span class="sxs-lookup"><span data-stu-id="bc181-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc181-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*朋 克*</span><span class="sxs-lookup"><span data-stu-id="bc181-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="bc181-110">指向檔案中的檔案或資料流程的 IAVI 介面指標。</span><span class="sxs-lookup"><span data-stu-id="bc181-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc181-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc181-111">Return Value</span></span>

<span data-ttu-id="bc181-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc181-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc181-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc181-113">Requirements</span></span>



| <span data-ttu-id="bc181-114">需求</span><span class="sxs-lookup"><span data-stu-id="bc181-114">Requirement</span></span> | <span data-ttu-id="bc181-115">值</span><span class="sxs-lookup"><span data-stu-id="bc181-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bc181-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc181-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc181-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc181-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bc181-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc181-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc181-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc181-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bc181-120">標頭</span><span class="sxs-lookup"><span data-stu-id="bc181-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc181-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc181-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc181-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc181-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc181-123">**MCIWndOpenInterface**</span><span class="sxs-lookup"><span data-stu-id="bc181-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





