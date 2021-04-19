---
description: 影片框架的寬度和高度（以圖元為單位）。
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: 'MF_MT_FRAME_SIZE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987811"
---
# <a name="mf_mt_frame_size-attribute"></a><span data-ttu-id="2d39d-103">MF \_ MT \_ 框架 \_ 大小屬性</span><span class="sxs-lookup"><span data-stu-id="2d39d-103">MF\_MT\_FRAME\_SIZE attribute</span></span>

<span data-ttu-id="2d39d-104">影片框架的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d39d-104">Width and height of a video frame, in pixels.</span></span>

## <a name="data-type"></a><span data-ttu-id="2d39d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2d39d-105">Data type</span></span>

<span data-ttu-id="2d39d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2d39d-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="2d39d-107">備註</span><span class="sxs-lookup"><span data-stu-id="2d39d-107">Remarks</span></span>

<span data-ttu-id="2d39d-108">上方的32位包含寬度，而較低的32位則包含高度。</span><span class="sxs-lookup"><span data-stu-id="2d39d-108">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="2d39d-109">若要設定此屬性，請使用 [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) 函數。</span><span class="sxs-lookup"><span data-stu-id="2d39d-109">To set this attribute, use the [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) function.</span></span> <span data-ttu-id="2d39d-110">若要取得這個屬性，請使用 [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) 函數。</span><span class="sxs-lookup"><span data-stu-id="2d39d-110">To get this attribute, use the [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) function.</span></span>

<span data-ttu-id="2d39d-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="2d39d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="2d39d-112">範例</span><span class="sxs-lookup"><span data-stu-id="2d39d-112">Examples</span></span>


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a><span data-ttu-id="2d39d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d39d-113">Requirements</span></span>



| <span data-ttu-id="2d39d-114">需求</span><span class="sxs-lookup"><span data-stu-id="2d39d-114">Requirement</span></span> | <span data-ttu-id="2d39d-115">值</span><span class="sxs-lookup"><span data-stu-id="2d39d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d39d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d39d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d39d-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d39d-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2d39d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d39d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d39d-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d39d-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2d39d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2d39d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d39d-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d39d-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d39d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d39d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d39d-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2d39d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2d39d-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2d39d-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2d39d-125">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="2d39d-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




