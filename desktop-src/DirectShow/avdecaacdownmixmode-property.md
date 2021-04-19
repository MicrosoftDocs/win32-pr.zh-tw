---
description: 指定 AAC 解碼器是否使用標準的 MPEG-2/MPEG-4 身歷聲 downmix 方程式，或使用非標準的 downmix。
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: 'AVDecAACDownmixMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972316"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="68c5a-103">AVDecAACDownmixMode 屬性</span><span class="sxs-lookup"><span data-stu-id="68c5a-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="68c5a-104">指定 AAC 解碼器是否使用標準的 MPEG-2/MPEG-4 身歷聲 downmix 方程式，或使用非標準的 downmix。</span><span class="sxs-lookup"><span data-stu-id="68c5a-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="68c5a-105">非標準 downmix 的範例，是由 ARIB 檔 STD-B21 4.4 版所定義。</span><span class="sxs-lookup"><span data-stu-id="68c5a-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="68c5a-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="68c5a-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="68c5a-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="68c5a-107">Data type</span></span>

<span data-ttu-id="68c5a-108">**UINT32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="68c5a-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="68c5a-109">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="68c5a-109">Property GUID</span></span>

<span data-ttu-id="68c5a-110">**CODECAPI \_ AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="68c5a-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="68c5a-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="68c5a-111">Property value</span></span>

<span data-ttu-id="68c5a-112">這個屬性的值是 [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="68c5a-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c5a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="68c5a-113">Requirements</span></span>



| <span data-ttu-id="68c5a-114">需求</span><span class="sxs-lookup"><span data-stu-id="68c5a-114">Requirement</span></span> | <span data-ttu-id="68c5a-115">值</span><span class="sxs-lookup"><span data-stu-id="68c5a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68c5a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68c5a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="68c5a-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68c5a-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="68c5a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68c5a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="68c5a-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68c5a-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="68c5a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="68c5a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="68c5a-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="68c5a-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c5a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68c5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c5a-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="68c5a-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="68c5a-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="68c5a-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

