---
title: 'MCIWNDM_VALIDATEMEDIA 訊息 (Vfw .h) '
description: MCIWNDM \_ VALIDATEMEDIA 訊息會根據目前時間格式，更新內容的開始和結束位置、內容中的目前位置，以及顯示的內容。
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508331"
---
# <a name="mciwndm_validatemedia-message"></a><span data-ttu-id="d371b-104">MCIWNDM \_ VALIDATEMEDIA 訊息</span><span class="sxs-lookup"><span data-stu-id="d371b-104">MCIWNDM\_VALIDATEMEDIA message</span></span>

<span data-ttu-id="d371b-105">**MCIWNDM \_ VALIDATEMEDIA** 訊息會根據目前時間格式，更新內容的開始和結束位置、內容中的目前位置，以及顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="d371b-105">The **MCIWNDM\_VALIDATEMEDIA** message updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.</span></span> <span data-ttu-id="d371b-106">您可以使用 [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d371b-106">You can send this message explicitly or by using the [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) macro.</span></span>


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d371b-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="d371b-107">Return Value</span></span>

<span data-ttu-id="d371b-108">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d371b-108">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d371b-109">備註</span><span class="sxs-lookup"><span data-stu-id="d371b-109">Remarks</span></span>

<span data-ttu-id="d371b-110">一般來說，您應該不需要使用這個宏。但是，如果您的應用程式在不使用 MCIWnd 的情況下變更裝置的時間格式;內容的開始和結束位置以及這些內容會繼續使用舊格式。</span><span class="sxs-lookup"><span data-stu-id="d371b-110">Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format.</span></span> <span data-ttu-id="d371b-111">您可以使用這個宏來更新這些值。</span><span class="sxs-lookup"><span data-stu-id="d371b-111">You can use this macro to update these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d371b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d371b-112">Requirements</span></span>



| <span data-ttu-id="d371b-113">需求</span><span class="sxs-lookup"><span data-stu-id="d371b-113">Requirement</span></span> | <span data-ttu-id="d371b-114">值</span><span class="sxs-lookup"><span data-stu-id="d371b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d371b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d371b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d371b-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d371b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d371b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d371b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d371b-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d371b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d371b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d371b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d371b-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="d371b-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d371b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d371b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d371b-122">**MCIWndValidateMedia**</span><span class="sxs-lookup"><span data-stu-id="d371b-122">**MCIWndValidateMedia**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





