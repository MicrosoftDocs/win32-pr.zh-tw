---
description: 指定輸入資料流程是否為交錯式。
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: 'MFPKEY_RESIZE_INTERLACE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981525"
---
# <a name="mfpkey_resize_interlace-property"></a><span data-ttu-id="45598-103">MFPKEY 重 \_ 設大小 \_ 交錯屬性</span><span class="sxs-lookup"><span data-stu-id="45598-103">MFPKEY\_RESIZE\_INTERLACE Property</span></span>

<span data-ttu-id="45598-104">指定輸入資料流程是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="45598-104">Specifies whether the input stream is interlaced.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="45598-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="45598-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="45598-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="45598-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="45598-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="45598-107">Data Type</span></span>

<span data-ttu-id="45598-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="45598-108">VT\_BOOL</span></span>

## <a name="applies-to"></a><span data-ttu-id="45598-109">套用至</span><span class="sxs-lookup"><span data-stu-id="45598-109">Applies To</span></span>

-   [<span data-ttu-id="45598-110">影片尺寸調整 DSP</span><span class="sxs-lookup"><span data-stu-id="45598-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="45598-111">備註</span><span class="sxs-lookup"><span data-stu-id="45598-111">Remarks</span></span>

<span data-ttu-id="45598-112">請使用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="45598-112">Use one of the following values:</span></span>



| <span data-ttu-id="45598-113">值</span><span class="sxs-lookup"><span data-stu-id="45598-113">Value</span></span>     | <span data-ttu-id="45598-114">描述</span><span class="sxs-lookup"><span data-stu-id="45598-114">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="45598-115">VT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="45598-115">VT\_FALSE</span></span> | <span data-ttu-id="45598-116">漸進式</span><span class="sxs-lookup"><span data-stu-id="45598-116">Progressive</span></span> |
| <span data-ttu-id="45598-117">VT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="45598-117">VT\_TRUE</span></span>  | <span data-ttu-id="45598-118">Interlaced</span><span class="sxs-lookup"><span data-stu-id="45598-118">Interlaced</span></span>  |



 

<span data-ttu-id="45598-119">如果未設定此屬性，則 DSP 會使用輸入媒體類型來判斷影片是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="45598-119">If this property is not set, the DSP uses the input media type to determine whether the video is interlaced.</span></span> <span data-ttu-id="45598-120">您可以設定這個屬性來覆寫媒體類型設定。</span><span class="sxs-lookup"><span data-stu-id="45598-120">You can set this property to override the media type setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="45598-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="45598-121">Requirements</span></span>



| <span data-ttu-id="45598-122">需求</span><span class="sxs-lookup"><span data-stu-id="45598-122">Requirement</span></span> | <span data-ttu-id="45598-123">值</span><span class="sxs-lookup"><span data-stu-id="45598-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45598-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45598-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45598-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45598-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="45598-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45598-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45598-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45598-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45598-128">標頭</span><span class="sxs-lookup"><span data-stu-id="45598-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="45598-129"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="45598-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45598-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45598-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45598-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="45598-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
