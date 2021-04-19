---
description: 讓 capture engine 使用具有使用規定限制的解碼器。
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: 'MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981481"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="3272d-103">MF \_ CAPTURE \_ ENGINE \_ 解碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="3272d-103">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="3272d-104">讓 capture engine 使用具有使用規定限制的解碼器。</span><span class="sxs-lookup"><span data-stu-id="3272d-104">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="3272d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3272d-105">Data type</span></span>

<span data-ttu-id="3272d-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="3272d-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="3272d-107">備註</span><span class="sxs-lookup"><span data-stu-id="3272d-107">Remarks</span></span>

<span data-ttu-id="3272d-108">這個屬性的值是 [*IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)介面的指標，由呼叫端所執行。</span><span class="sxs-lookup"><span data-stu-id="3272d-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="3272d-109">呼叫端的這個介面的實作為預期會使用與解碼器的交握，如 [使用限制的欄位](field-of-use-restrictions.md)所述。</span><span class="sxs-lookup"><span data-stu-id="3272d-109">The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="3272d-110">Microsoft 媒體基礎不會定義交握，通常會牽涉到某種類型的密碼編譯交換。</span><span class="sxs-lookup"><span data-stu-id="3272d-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="3272d-111">就內部而言，capture 引擎會設定解碼器的 [MFT \_ FIELDOFUSE \_ UNLOCK \_ attribute](mft-fieldofuse-unlock-attribute.md)屬性，以設定 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)上的指標。</span><span class="sxs-lookup"><span data-stu-id="3272d-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="3272d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3272d-112">Requirements</span></span>



| <span data-ttu-id="3272d-113">需求</span><span class="sxs-lookup"><span data-stu-id="3272d-113">Requirement</span></span> | <span data-ttu-id="3272d-114">值</span><span class="sxs-lookup"><span data-stu-id="3272d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3272d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3272d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3272d-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3272d-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3272d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3272d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3272d-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3272d-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3272d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3272d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3272d-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3272d-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3272d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3272d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3272d-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3272d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3272d-123">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="3272d-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="3272d-124">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="3272d-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




