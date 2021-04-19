---
description: 設定 ASF 媒體來源在執行反復搜尋時，所要使用的搜尋反復專案數目上限。
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: 'MFPKEY_ASFMediaSource_IterativeSeek_Max_Count 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985817"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a><span data-ttu-id="3663c-103">MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count 屬性</span><span class="sxs-lookup"><span data-stu-id="3663c-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count property</span></span>

<span data-ttu-id="3663c-104">設定 ASF 媒體來源在執行反復搜尋時，所要使用的搜尋反復專案數目上限。</span><span class="sxs-lookup"><span data-stu-id="3663c-104">Sets the maximum number of search iterations the ASF media source will use when it performs iterative seeking.</span></span>



<span data-ttu-id="3663c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3663c-105">Data type</span></span>

<span data-ttu-id="3663c-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="3663c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3663c-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="3663c-107">PROPVARIANT member</span></span>

<span data-ttu-id="3663c-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="3663c-108">**ULONG**</span></span>

<span data-ttu-id="3663c-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="3663c-109">VT\_UI4</span></span>

<span data-ttu-id="3663c-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="3663c-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3663c-111">備註</span><span class="sxs-lookup"><span data-stu-id="3663c-111">Remarks</span></span>

<span data-ttu-id="3663c-112">使用這個屬性來設定 ASF 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="3663c-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="3663c-113">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="3663c-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="3663c-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="3663c-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="3663c-115">只有在已啟用反復搜尋時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="3663c-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="3663c-116">如需詳細資訊，請參閱 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md)。</span><span class="sxs-lookup"><span data-stu-id="3663c-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="3663c-117">這個屬性的有效範圍是 \[ 1-10 \] （含）。</span><span class="sxs-lookup"><span data-stu-id="3663c-117">The valid range of this property is \[1-10\], inclusive.</span></span> <span data-ttu-id="3663c-118">使用較高的數位，反復的搜尋通常更準確，但需要較長的時間。</span><span class="sxs-lookup"><span data-stu-id="3663c-118">With a higher number, iterative seeking tends to be more accurate but takes longer.</span></span>

<span data-ttu-id="3663c-119">預設值為 5。</span><span class="sxs-lookup"><span data-stu-id="3663c-119">The default value is 5.</span></span>

## <a name="requirements"></a><span data-ttu-id="3663c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3663c-120">Requirements</span></span>



| <span data-ttu-id="3663c-121">需求</span><span class="sxs-lookup"><span data-stu-id="3663c-121">Requirement</span></span> | <span data-ttu-id="3663c-122">值</span><span class="sxs-lookup"><span data-stu-id="3663c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3663c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3663c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3663c-124">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3663c-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3663c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3663c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3663c-126">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3663c-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3663c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3663c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3663c-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3663c-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3663c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3663c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3663c-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3663c-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




