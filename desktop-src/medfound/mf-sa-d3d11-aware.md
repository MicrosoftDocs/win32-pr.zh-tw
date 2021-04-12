---
description: 指定媒體基礎轉換 (MFT) 是否支援 Microsoft Direct3D 11。
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: 'MF_SA_D3D11_AWARE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318647"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="6db44-103">MF \_ SA \_ D3D11 \_ 感知屬性</span><span class="sxs-lookup"><span data-stu-id="6db44-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="6db44-104">指定媒體基礎轉換 (MFT) 是否支援 Microsoft Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="6db44-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="6db44-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6db44-105">Data type</span></span>

<span data-ttu-id="6db44-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="6db44-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6db44-107">備註</span><span class="sxs-lookup"><span data-stu-id="6db44-107">Remarks</span></span>

<span data-ttu-id="6db44-108">這個屬性只適用于影片 MFTs。</span><span class="sxs-lookup"><span data-stu-id="6db44-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="6db44-109">若要查詢這個屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="6db44-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="6db44-110">如果 **GetAttributes** 成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="6db44-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="6db44-111">如果屬性為非零，用戶端可以在串流處理開始之前，為 MFT 提供 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6db44-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="6db44-112">若要這樣做，用戶端會將 [**mft \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。</span><span class="sxs-lookup"><span data-stu-id="6db44-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="6db44-113">用戶端不需要傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6db44-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="6db44-114">如果此屬性為零 (**FALSE**) ，則 MFT 不支援 Direct3D 11，而且用戶端不應該將 [**mft \_ 訊息集的 \_ \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。</span><span class="sxs-lookup"><span data-stu-id="6db44-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="6db44-115">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6db44-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="6db44-116">將此屬性視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="6db44-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="6db44-117">請勿變更值;MFT 會忽略值的任何變更。</span><span class="sxs-lookup"><span data-stu-id="6db44-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db44-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6db44-118">Requirements</span></span>



| <span data-ttu-id="6db44-119">需求</span><span class="sxs-lookup"><span data-stu-id="6db44-119">Requirement</span></span> | <span data-ttu-id="6db44-120">值</span><span class="sxs-lookup"><span data-stu-id="6db44-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db44-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6db44-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6db44-122">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6db44-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6db44-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6db44-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6db44-124">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6db44-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6db44-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6db44-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db44-126"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="6db44-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db44-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6db44-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db44-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6db44-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6db44-129">支援媒體基礎中的 Direct3D 11 影片解碼</span><span class="sxs-lookup"><span data-stu-id="6db44-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




