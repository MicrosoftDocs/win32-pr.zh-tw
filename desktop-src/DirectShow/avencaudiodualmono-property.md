---
description: AVEncAudioDualMono 屬性-指定雙聲道音訊是否編碼為身歷聲或雙 mono。
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: 'AVEncAudioDualMono 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096576"
---
# <a name="avencaudiodualmono-property"></a><span data-ttu-id="bd51d-103">AVEncAudioDualMono 屬性</span><span class="sxs-lookup"><span data-stu-id="bd51d-103">AVEncAudioDualMono property</span></span>

<span data-ttu-id="bd51d-104">指定雙聲道音訊是否編碼為身歷聲或雙 mono。</span><span class="sxs-lookup"><span data-stu-id="bd51d-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="bd51d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd51d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bd51d-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="bd51d-106">Data type</span></span>

<span data-ttu-id="bd51d-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="bd51d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bd51d-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="bd51d-108">Property GUID</span></span>

<span data-ttu-id="bd51d-109">**CODECAPI \_ AVEncAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="bd51d-109">**CODECAPI\_AVEncAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="bd51d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd51d-110">Property value</span></span>

<span data-ttu-id="bd51d-111">這個屬性的值是 [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="bd51d-111">The value of this property is a member of the [**eAVEncAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd51d-112">備註</span><span class="sxs-lookup"><span data-stu-id="bd51d-112">Remarks</span></span>

<span data-ttu-id="bd51d-113">此屬性不適用於 MPEG 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="bd51d-113">This property does not apply to MPEG audio encoders.</span></span> <span data-ttu-id="bd51d-114">若為 MPEG 音訊，請使用 [**AVEncMPACodingMode**](avencmpacodingmode-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="bd51d-114">For MPEG audio, use the [**AVEncMPACodingMode**](avencmpacodingmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd51d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd51d-115">Requirements</span></span>



| <span data-ttu-id="bd51d-116">需求</span><span class="sxs-lookup"><span data-stu-id="bd51d-116">Requirement</span></span> | <span data-ttu-id="bd51d-117">值</span><span class="sxs-lookup"><span data-stu-id="bd51d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd51d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd51d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd51d-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd51d-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bd51d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd51d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd51d-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd51d-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bd51d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bd51d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd51d-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd51d-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd51d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd51d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd51d-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="bd51d-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bd51d-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="bd51d-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

