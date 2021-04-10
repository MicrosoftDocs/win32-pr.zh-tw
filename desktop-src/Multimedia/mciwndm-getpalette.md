---
title: 'MCIWNDM_GETPALETTE 訊息 (Vfw .h) '
description: MCIWNDM \_ GETPALETTE 訊息會抓取 MCI 裝置所使用的調色板控制碼。 您可以使用 MCIWndGetPalette 宏明確地傳送此訊息。
ms.assetid: f8426344-0fee-4419-9d8a-dcee26cb4c28
keywords:
- MCIWNDM_GETPALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faec3dd5d9c401d943fbc55ca58e452d3fb25497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024704"
---
# <a name="mciwndm_getpalette-message"></a><span data-ttu-id="85c44-105">MCIWNDM \_ GETPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="85c44-105">MCIWNDM\_GETPALETTE message</span></span>

<span data-ttu-id="85c44-106">**MCIWNDM \_ GETPALETTE** 訊息會抓取 MCI 裝置所使用的調色板控制碼。</span><span class="sxs-lookup"><span data-stu-id="85c44-106">The **MCIWNDM\_GETPALETTE** message retrieves a handle of the palette used by an MCI device.</span></span> <span data-ttu-id="85c44-107">您可以使用 [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="85c44-107">You can send this message explicitly or by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span>


```C++
MCIWNDM_GETPALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="85c44-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="85c44-108">Return Value</span></span>

<span data-ttu-id="85c44-109">如果成功，則傳回檔色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="85c44-109">Returns the handle of the palette if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c44-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="85c44-110">Requirements</span></span>



| <span data-ttu-id="85c44-111">需求</span><span class="sxs-lookup"><span data-stu-id="85c44-111">Requirement</span></span> | <span data-ttu-id="85c44-112">值</span><span class="sxs-lookup"><span data-stu-id="85c44-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="85c44-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85c44-113">Minimum supported client</span></span><br/> | <span data-ttu-id="85c44-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85c44-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="85c44-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85c44-115">Minimum supported server</span></span><br/> | <span data-ttu-id="85c44-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85c44-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="85c44-117">標頭</span><span class="sxs-lookup"><span data-stu-id="85c44-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c44-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="85c44-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c44-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85c44-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c44-120">**MCIWndGetPalette**</span><span class="sxs-lookup"><span data-stu-id="85c44-120">**MCIWndGetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
</dt> </dl>

 

 





