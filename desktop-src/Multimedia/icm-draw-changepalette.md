---
title: 'ICM_DRAW_CHANGEPALETTE 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ CHANGEPALETTE 訊息會通知轉譯驅動程式，表示電影調色板正在變更。 您可以使用 ICDrawChangePalette 宏明確地傳送此訊息。
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843756"
---
# <a name="icm_draw_changepalette-message"></a><span data-ttu-id="7fcfe-105">ICM \_ 繪圖 \_ CHANGEPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="7fcfe-105">ICM\_DRAW\_CHANGEPALETTE message</span></span>

<span data-ttu-id="7fcfe-106">**ICM \_ DRAW \_ CHANGEPALETTE** 訊息會通知轉譯驅動程式，表示電影調色板正在變更。</span><span class="sxs-lookup"><span data-stu-id="7fcfe-106">The **ICM\_DRAW\_CHANGEPALETTE** message notifies a rendering driver that the movie palette is changing.</span></span> <span data-ttu-id="7fcfe-107">您可以使用 [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="7fcfe-107">You can send this message explicitly or by using the [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) macro.</span></span>


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7fcfe-108">參數</span><span class="sxs-lookup"><span data-stu-id="7fcfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcfe-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="7fcfe-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="7fcfe-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含新的格式和選擇性色彩表。</span><span class="sxs-lookup"><span data-stu-id="7fcfe-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the new format and optional color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcfe-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fcfe-111">Return Value</span></span>

<span data-ttu-id="7fcfe-112">\_如果成功則傳回 ICERR OK，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7fcfe-112">Returns ICERR\_OK if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fcfe-113">備註</span><span class="sxs-lookup"><span data-stu-id="7fcfe-113">Remarks</span></span>

<span data-ttu-id="7fcfe-114">這則訊息應該由可安裝的轉譯處理常式所支援，這些處理常式會使用包含調色板的內部結構來繪製 Dib。</span><span class="sxs-lookup"><span data-stu-id="7fcfe-114">This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcfe-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fcfe-115">Requirements</span></span>



| <span data-ttu-id="7fcfe-116">需求</span><span class="sxs-lookup"><span data-stu-id="7fcfe-116">Requirement</span></span> | <span data-ttu-id="7fcfe-117">值</span><span class="sxs-lookup"><span data-stu-id="7fcfe-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fcfe-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7fcfe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcfe-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fcfe-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7fcfe-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7fcfe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcfe-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7fcfe-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7fcfe-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7fcfe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcfe-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfe-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcfe-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fcfe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcfe-125">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="7fcfe-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7fcfe-126">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="7fcfe-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

