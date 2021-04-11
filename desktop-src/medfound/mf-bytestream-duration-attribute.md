---
description: 指定位元組資料流程的持續時間，以 100-毫微秒單位表示。
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: 'MF_BYTESTREAM_DURATION 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318811"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="a4134-103">MF \_ BYTESTREAM \_ DURATION 屬性</span><span class="sxs-lookup"><span data-stu-id="a4134-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="a4134-104">指定位元組資料流程的持續時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="a4134-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4134-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a4134-105">Data type</span></span>

<span data-ttu-id="a4134-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a4134-106">**UINT64**</span></span>

<span data-ttu-id="a4134-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="a4134-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4134-108">備註</span><span class="sxs-lookup"><span data-stu-id="a4134-108">Remarks</span></span>

<span data-ttu-id="a4134-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a4134-109">This attribute is optional.</span></span> <span data-ttu-id="a4134-110">如果建立位元組資料流程的物件可以判斷持續時間，則可以設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a4134-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="a4134-111"> (例如，在網路資料流程中，持續時間可能是會話描述的一部分。 ) </span><span class="sxs-lookup"><span data-stu-id="a4134-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="a4134-112">若要取得屬性值，請呼叫位元組資料流程上的 **QueryInterface** 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a4134-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="a4134-113">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="a4134-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="a4134-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a4134-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4134-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4134-115">Requirements</span></span>



| <span data-ttu-id="a4134-116">需求</span><span class="sxs-lookup"><span data-stu-id="a4134-116">Requirement</span></span> | <span data-ttu-id="a4134-117">值</span><span class="sxs-lookup"><span data-stu-id="a4134-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4134-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4134-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a4134-119">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4134-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="a4134-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4134-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a4134-121">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4134-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a4134-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a4134-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4134-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="a4134-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4134-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4134-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4134-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a4134-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4134-126">位元組資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="a4134-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4134-127">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="a4134-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="a4134-128">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="a4134-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="a4134-129">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="a4134-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




