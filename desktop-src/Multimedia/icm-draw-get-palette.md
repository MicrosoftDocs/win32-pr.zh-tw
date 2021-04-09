---
title: 'ICM_DRAW_GET_PALETTE 訊息 (Vfw .h) '
description: ICM \_ 繪圖 \_ GET \_ 調色板訊息要求轉譯驅動程式傳回檔色板。
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024711"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="fa2fd-104">ICM \_ 繪圖 \_ 取得 \_ 調色板訊息</span><span class="sxs-lookup"><span data-stu-id="fa2fd-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="fa2fd-105">**ICM \_ 繪圖 \_ GET \_ 調色板** 訊息要求轉譯驅動程式傳回檔色板。</span><span class="sxs-lookup"><span data-stu-id="fa2fd-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="fa2fd-106">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa2fd-106">Return Value</span></span>

<span data-ttu-id="fa2fd-107">驅動程式應該會傳回下列其中一項：所使用之調色板的控制碼、 **Null** （如果沒有要傳回的控制碼）或 ICERR 不 \_ 支援調色板時不支援。</span><span class="sxs-lookup"><span data-stu-id="fa2fd-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2fd-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa2fd-108">Requirements</span></span>



| <span data-ttu-id="fa2fd-109">需求</span><span class="sxs-lookup"><span data-stu-id="fa2fd-109">Requirement</span></span> | <span data-ttu-id="fa2fd-110">值</span><span class="sxs-lookup"><span data-stu-id="fa2fd-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa2fd-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa2fd-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2fd-112">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa2fd-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fa2fd-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa2fd-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2fd-114">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa2fd-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa2fd-115">標頭</span><span class="sxs-lookup"><span data-stu-id="fa2fd-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2fd-116"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2fd-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa2fd-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa2fd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2fd-118">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="fa2fd-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="fa2fd-119">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="fa2fd-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





