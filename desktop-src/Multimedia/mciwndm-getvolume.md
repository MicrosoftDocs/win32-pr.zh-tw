---
title: 'MCIWNDM_GETVOLUME 訊息 (Vfw .h) '
description: MCIWNDM \_ GETVOLUME 訊息會抓取 MCI 裝置目前的磁片區設定。 您可以使用 MCIWndGetVolume 宏明確地傳送此訊息。
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385194"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="a1a0c-105">MCIWNDM \_ GETVOLUME 訊息</span><span class="sxs-lookup"><span data-stu-id="a1a0c-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="a1a0c-106">**MCIWNDM \_ GETVOLUME** 訊息會抓取 MCI 裝置目前的磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="a1a0c-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="a1a0c-107">您可以使用 [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a1a0c-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="a1a0c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1a0c-108">Return Value</span></span>

<span data-ttu-id="a1a0c-109">傳回目前的磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="a1a0c-109">Returns the current volume setting.</span></span> <span data-ttu-id="a1a0c-110">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="a1a0c-110">The default value is 1000.</span></span> <span data-ttu-id="a1a0c-111">較高的值表示較大的磁片區，較低的值表示更快的磁片</span><span class="sxs-lookup"><span data-stu-id="a1a0c-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a0c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1a0c-112">Requirements</span></span>



| <span data-ttu-id="a1a0c-113">需求</span><span class="sxs-lookup"><span data-stu-id="a1a0c-113">Requirement</span></span> | <span data-ttu-id="a1a0c-114">值</span><span class="sxs-lookup"><span data-stu-id="a1a0c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a1a0c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1a0c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a0c-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1a0c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a1a0c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1a0c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a0c-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1a0c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1a0c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="a1a0c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1a0c-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a0c-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1a0c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1a0c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a0c-122">**MCIWndGetVolume**</span><span class="sxs-lookup"><span data-stu-id="a1a0c-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





