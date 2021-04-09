---
description: 指定 &\# 0034; 有漏洞 bucket&\# 0034; ASF 媒體接收器上的資料流程參數。
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: 'MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848209"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="9aaac-103">MFPKEY \_ ASFSTREAMSINK 已 \_ 更正的 \_ LEAKYBUCKET 屬性</span><span class="sxs-lookup"><span data-stu-id="9aaac-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="9aaac-104">指定 "有漏洞 bucket" 參數 (查看 ASF 媒體接收器上資料流程的備註) 。</span><span class="sxs-lookup"><span data-stu-id="9aaac-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="9aaac-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9aaac-105">Data type</span></span>

<span data-ttu-id="9aaac-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="9aaac-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9aaac-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="9aaac-107">PROPVARIANT member</span></span>

<span data-ttu-id="9aaac-108">**DWORD** 值的陣列 (**CAUL**) </span><span class="sxs-lookup"><span data-stu-id="9aaac-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="9aaac-109">VT \_ 向量 \| vt \_ UI4</span><span class="sxs-lookup"><span data-stu-id="9aaac-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="9aaac-110">**科爾**</span><span class="sxs-lookup"><span data-stu-id="9aaac-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="9aaac-111">備註</span><span class="sxs-lookup"><span data-stu-id="9aaac-111">Remarks</span></span>

<span data-ttu-id="9aaac-112">應用程式可以在資料流程的媒體類型經過協商之後，于 ASF 媒體接收器的資料流程上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="9aaac-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="9aaac-113">您可以使用這個屬性來指定 Windows Media 編解碼器將使用的實際緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="9aaac-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="9aaac-114">您可以使用 Windows Media Format SDK 中記載的 **IWMCodecLeakyBucket** 介面，從編解碼器取得這項資訊。</span><span class="sxs-lookup"><span data-stu-id="9aaac-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="9aaac-115">這個屬性的值是下列順序的三個 **DWORD** 值的陣列：</span><span class="sxs-lookup"><span data-stu-id="9aaac-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="9aaac-116">位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="9aaac-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="9aaac-117">緩衝區大小，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="9aaac-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="9aaac-118">初始緩衝區飽和度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9aaac-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aaac-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9aaac-119">Requirements</span></span>



| <span data-ttu-id="9aaac-120">需求</span><span class="sxs-lookup"><span data-stu-id="9aaac-120">Requirement</span></span> | <span data-ttu-id="9aaac-121">值</span><span class="sxs-lookup"><span data-stu-id="9aaac-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9aaac-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9aaac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9aaac-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aaac-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9aaac-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9aaac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9aaac-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9aaac-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9aaac-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9aaac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aaac-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9aaac-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aaac-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9aaac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aaac-129">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="9aaac-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="9aaac-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9aaac-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




