---
title: 'MCIWNDM_SETPALETTE 訊息 (Vfw .h) '
description: MCIWNDM \_ SETPALETTE 訊息會將調色板控制碼傳送至與 MCIWnd 視窗相關聯的 MCI 裝置。 您可以使用 MCIWndSetPalette 宏明確地傳送此訊息。
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e354082de4fc15f4179555a8b635b9426af90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466049"
---
# <a name="mciwndm_setpalette-message"></a><span data-ttu-id="eb34e-105">MCIWNDM \_ SETPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="eb34e-105">MCIWNDM\_SETPALETTE message</span></span>

<span data-ttu-id="eb34e-106">**MCIWNDM \_ SETPALETTE** 訊息會將調色板控制碼傳送至與 MCIWnd 視窗相關聯的 MCI 裝置。</span><span class="sxs-lookup"><span data-stu-id="eb34e-106">The **MCIWNDM\_SETPALETTE** message sends a palette handle to the MCI device associated with the MCIWnd window.</span></span> <span data-ttu-id="eb34e-107">您可以使用 [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="eb34e-107">You can send this message explicitly or by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="eb34e-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb34e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb34e-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span><span class="sxs-lookup"><span data-stu-id="eb34e-109"><span id="hpal"></span><span id="HPAL"></span>*hpal*</span></span>
</dt> <dd>

<span data-ttu-id="eb34e-110">調色板控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb34e-110">Palette handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb34e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb34e-111">Return Value</span></span>

<span data-ttu-id="eb34e-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb34e-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb34e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb34e-113">Requirements</span></span>



| <span data-ttu-id="eb34e-114">需求</span><span class="sxs-lookup"><span data-stu-id="eb34e-114">Requirement</span></span> | <span data-ttu-id="eb34e-115">值</span><span class="sxs-lookup"><span data-stu-id="eb34e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eb34e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb34e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eb34e-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb34e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eb34e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb34e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eb34e-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb34e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eb34e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="eb34e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb34e-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb34e-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb34e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb34e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb34e-123">**MCIWndSetPalette**</span><span class="sxs-lookup"><span data-stu-id="eb34e-123">**MCIWndSetPalette**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





