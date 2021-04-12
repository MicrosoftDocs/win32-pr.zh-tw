---
description: 讓 capture engine 使用具有使用規定限制的編碼器。
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: 'MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191900"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="bc589-103">MF \_ 捕獲 \_ 引擎 \_ 編碼器 \_ MFT \_ FIELDOFUSE \_ 解除鎖定 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="bc589-103">MF\_CAPTURE\_ENGINE\_ENCODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="bc589-104">讓 capture engine 使用具有使用規定限制的編碼器。</span><span class="sxs-lookup"><span data-stu-id="bc589-104">Enables the capture engine to use an encoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="bc589-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bc589-105">Data type</span></span>

<span data-ttu-id="bc589-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="bc589-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="bc589-107">備註</span><span class="sxs-lookup"><span data-stu-id="bc589-107">Remarks</span></span>

<span data-ttu-id="bc589-108">這個屬性的值是 [*IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)介面的指標，由呼叫端所執行。</span><span class="sxs-lookup"><span data-stu-id="bc589-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="bc589-109">此介面的呼叫端必須執行與編碼器的交握，如 [使用限制的欄位](field-of-use-restrictions.md)所述。</span><span class="sxs-lookup"><span data-stu-id="bc589-109">The caller's implementation of this interface is expected to perform a handshake with the encoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="bc589-110">Microsoft 媒體基礎不會定義交握，通常會牽涉到某種類型的密碼編譯交換。</span><span class="sxs-lookup"><span data-stu-id="bc589-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="bc589-111">就內部而言，capture 引擎會設定編碼器的 [MFT \_ FIELDOFUSE \_ UNLOCK \_ attribute](mft-fieldofuse-unlock-attribute.md)屬性來設定編碼器上的 [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)指標。</span><span class="sxs-lookup"><span data-stu-id="bc589-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the encoder by setting the encoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc589-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc589-112">Requirements</span></span>



| <span data-ttu-id="bc589-113">需求</span><span class="sxs-lookup"><span data-stu-id="bc589-113">Requirement</span></span> | <span data-ttu-id="bc589-114">值</span><span class="sxs-lookup"><span data-stu-id="bc589-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc589-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc589-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bc589-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc589-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bc589-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc589-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bc589-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc589-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bc589-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bc589-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc589-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc589-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc589-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc589-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc589-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bc589-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc589-123">Capture 引擎屬性</span><span class="sxs-lookup"><span data-stu-id="bc589-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc589-124">**IMFCaptureEngine：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="bc589-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




