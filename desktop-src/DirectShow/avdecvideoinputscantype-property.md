---
description: 指定已解碼的影片資料流程如何交錯。
ms.assetid: a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c
title: 'AVDecVideoInputScanType 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 560db1cd1cf0238fc9e50257f2f24559e9a94c8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846551"
---
# <a name="avdecvideoinputscantype-property"></a><span data-ttu-id="7e260-103">AVDecVideoInputScanType 屬性</span><span class="sxs-lookup"><span data-stu-id="7e260-103">AVDecVideoInputScanType property</span></span>

<span data-ttu-id="7e260-104">指定已解碼的影片資料流程如何交錯。</span><span class="sxs-lookup"><span data-stu-id="7e260-104">Specifies how the decoded video stream is interlaced.</span></span>

<span data-ttu-id="7e260-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="7e260-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e260-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="7e260-106">Data type</span></span>

<span data-ttu-id="7e260-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="7e260-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7e260-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="7e260-108">Property GUID</span></span>

<span data-ttu-id="7e260-109">**CODECAPI \_ AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="7e260-109">**CODECAPI\_AVDecVideoInputScanType**</span></span>

## <a name="property-value"></a><span data-ttu-id="7e260-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="7e260-110">Property value</span></span>

<span data-ttu-id="7e260-111">這個屬性的值是 [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="7e260-111">The value of this property is a member of the [**eAVDecVideoInputScanType**](/windows/win32/api/codecapi/ne-codecapi-eavdecvideoinputscantype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e260-112">備註</span><span class="sxs-lookup"><span data-stu-id="7e260-112">Remarks</span></span>

<span data-ttu-id="7e260-113">值的上層16位包含寬度，而較低的16位則包含高度。</span><span class="sxs-lookup"><span data-stu-id="7e260-113">The upper 16 bits of the value contain the width, and the lower 16 bits contain the height.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e260-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e260-114">Requirements</span></span>



| <span data-ttu-id="7e260-115">需求</span><span class="sxs-lookup"><span data-stu-id="7e260-115">Requirement</span></span> | <span data-ttu-id="7e260-116">值</span><span class="sxs-lookup"><span data-stu-id="7e260-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e260-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e260-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e260-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e260-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7e260-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e260-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e260-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e260-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7e260-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7e260-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e260-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e260-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e260-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e260-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e260-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="7e260-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7e260-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="7e260-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

