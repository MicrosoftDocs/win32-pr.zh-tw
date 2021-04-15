---
title: 'MCIWNDM_GETSTART 訊息 (Vfw .h) '
description: MCIWNDM \_ GETSTART 訊息會抓取 MCI 裝置或檔案的內容開頭位置。 您可以使用 MCIWndGetStart 宏明確地傳送此訊息。
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464513"
---
# <a name="mciwndm_getstart-message"></a><span data-ttu-id="e2e9b-105">MCIWNDM \_ GETSTART 訊息</span><span class="sxs-lookup"><span data-stu-id="e2e9b-105">MCIWNDM\_GETSTART message</span></span>

<span data-ttu-id="e2e9b-106">**MCIWNDM \_ GETSTART** 訊息會抓取 MCI 裝置或檔案的內容開頭位置。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-106">The **MCIWNDM\_GETSTART** message retrieves the location of the beginning of the content of an MCI device or file.</span></span> <span data-ttu-id="e2e9b-107">您可以使用 [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-107">You can send this message explicitly or by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) macro.</span></span>


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="e2e9b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2e9b-108">Return Value</span></span>

<span data-ttu-id="e2e9b-109">傳回目前時間格式的位置。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-109">Returns the location in the current time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e9b-110">備註</span><span class="sxs-lookup"><span data-stu-id="e2e9b-110">Remarks</span></span>

<span data-ttu-id="e2e9b-111">通常，傳回值為零。但有些裝置使用非零的起始位置。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-111">Typically, the return value is zero; but some devices use a nonzero starting location.</span></span> <span data-ttu-id="e2e9b-112">搜尋此位置會將裝置設定為媒體的開頭。</span><span class="sxs-lookup"><span data-stu-id="e2e9b-112">Seeking to this location sets the device to the start of the media.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e9b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2e9b-113">Requirements</span></span>



| <span data-ttu-id="e2e9b-114">需求</span><span class="sxs-lookup"><span data-stu-id="e2e9b-114">Requirement</span></span> | <span data-ttu-id="e2e9b-115">值</span><span class="sxs-lookup"><span data-stu-id="e2e9b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2e9b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2e9b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e9b-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2e9b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e2e9b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2e9b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e9b-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2e9b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e2e9b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e2e9b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e9b-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e9b-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e9b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2e9b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e9b-123">**MCIWndGetStart**</span><span class="sxs-lookup"><span data-stu-id="e2e9b-123">**MCIWndGetStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





