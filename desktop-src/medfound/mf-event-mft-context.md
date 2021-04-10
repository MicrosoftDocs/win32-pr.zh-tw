---
description: 包含 METransformMarker 事件的呼叫端定義值。
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: 'MF_EVENT_MFT_CONTEXT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026446"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="68139-103">MF \_ 事件 \_ MFT \_ 內容屬性</span><span class="sxs-lookup"><span data-stu-id="68139-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="68139-104">包含 [METransformMarker](metransformmarker.md) 事件的呼叫端定義值。</span><span class="sxs-lookup"><span data-stu-id="68139-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="68139-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="68139-105">Data type</span></span>

<span data-ttu-id="68139-106">**ULONG \_** 以 **UINT64** 形式儲存的 PTR</span><span class="sxs-lookup"><span data-stu-id="68139-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="68139-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="68139-107">Get/set</span></span>

<span data-ttu-id="68139-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="68139-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="68139-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="68139-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="68139-110">適用於</span><span class="sxs-lookup"><span data-stu-id="68139-110">Applies to</span></span>

[<span data-ttu-id="68139-111">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="68139-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="68139-112">備註</span><span class="sxs-lookup"><span data-stu-id="68139-112">Remarks</span></span>

<span data-ttu-id="68139-113">這個屬性會與 [METransformMarker](metransformmarker.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="68139-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="68139-114">屬性的值取自 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)方法的 *ulParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="68139-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="68139-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="68139-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68139-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="68139-116">Requirements</span></span>



| <span data-ttu-id="68139-117">需求</span><span class="sxs-lookup"><span data-stu-id="68139-117">Requirement</span></span> | <span data-ttu-id="68139-118">值</span><span class="sxs-lookup"><span data-stu-id="68139-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68139-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68139-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68139-120">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68139-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="68139-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68139-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68139-122">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68139-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="68139-123">標頭</span><span class="sxs-lookup"><span data-stu-id="68139-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68139-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="68139-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68139-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68139-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68139-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="68139-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68139-127">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="68139-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="68139-128">事件屬性</span><span class="sxs-lookup"><span data-stu-id="68139-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




