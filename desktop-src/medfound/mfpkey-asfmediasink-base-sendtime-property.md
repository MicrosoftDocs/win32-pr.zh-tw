---
description: ASF 媒體接收器的基底傳送時間（以毫秒為單位）。
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: 'MFPKEY_ASFMEDIASINK_BASE_SENDTIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992639"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="e6079-103">MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME 屬性</span><span class="sxs-lookup"><span data-stu-id="e6079-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="e6079-104">ASF 媒體接收器的基底傳送時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e6079-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="e6079-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e6079-105">Data type</span></span>

<span data-ttu-id="e6079-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="e6079-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e6079-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="e6079-107">PROPVARIANT member</span></span>

<span data-ttu-id="e6079-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="e6079-108">**ULONG**</span></span>

<span data-ttu-id="e6079-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e6079-109">VT\_UI4</span></span>

<span data-ttu-id="e6079-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="e6079-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e6079-111">備註</span><span class="sxs-lookup"><span data-stu-id="e6079-111">Remarks</span></span>

<span data-ttu-id="e6079-112">傳送時間是在網路上傳送 ASF 封包的時間。</span><span class="sxs-lookup"><span data-stu-id="e6079-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="e6079-113">它不會直接對應至封包中資料的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="e6079-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="e6079-114">您可以使用這個屬性來設定 ASF 媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="e6079-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="e6079-115">使用方式取決於您所呼叫用來建立 ASF 媒體接收器的函式：</span><span class="sxs-lookup"><span data-stu-id="e6079-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="e6079-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：查詢 **IPropertyStore** 介面的已取出 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)指標。</span><span class="sxs-lookup"><span data-stu-id="e6079-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="e6079-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)：在 *pContentInfo* 參數中指定的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。</span><span class="sxs-lookup"><span data-stu-id="e6079-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6079-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6079-118">Requirements</span></span>



| <span data-ttu-id="e6079-119">需求</span><span class="sxs-lookup"><span data-stu-id="e6079-119">Requirement</span></span> | <span data-ttu-id="e6079-120">值</span><span class="sxs-lookup"><span data-stu-id="e6079-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6079-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6079-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e6079-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6079-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e6079-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6079-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e6079-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6079-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e6079-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e6079-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6079-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6079-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6079-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6079-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6079-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e6079-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




