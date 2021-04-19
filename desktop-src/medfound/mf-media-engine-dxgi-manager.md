---
description: 設定媒體引擎上的 Microsoft DirectX Graphic Infrastructure (DXGI) 裝置管理員。
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: 'MF_MEDIA_ENGINE_DXGI_MANAGER 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981733"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="b2803-103">MF \_ 媒體 \_ 引擎 \_ DXGI \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="b2803-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="b2803-104">設定媒體引擎上的 Microsoft DirectX Graphic Infrastructure (DXGI) 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="b2803-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="b2803-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b2803-105">Data type</span></span>

<span data-ttu-id="b2803-106">**IMFDXGIDeviceManager \* *_ 儲存為 _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="b2803-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="b2803-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b2803-107">Get/set</span></span>

<span data-ttu-id="b2803-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="b2803-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="b2803-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="b2803-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2803-110">備註</span><span class="sxs-lookup"><span data-stu-id="b2803-110">Remarks</span></span>

<span data-ttu-id="b2803-111">這個屬性的值是 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b2803-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="b2803-112">在框架伺服器模式中，此屬性可讓媒體引擎使用硬體加速進行影片解碼和影片處理。</span><span class="sxs-lookup"><span data-stu-id="b2803-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="b2803-113">如果未設定此屬性，則媒體引擎會使用軟體解碼和處理。</span><span class="sxs-lookup"><span data-stu-id="b2803-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2803-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2803-114">Requirements</span></span>



| <span data-ttu-id="b2803-115">需求</span><span class="sxs-lookup"><span data-stu-id="b2803-115">Requirement</span></span> | <span data-ttu-id="b2803-116">值</span><span class="sxs-lookup"><span data-stu-id="b2803-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2803-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2803-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b2803-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2803-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="b2803-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2803-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b2803-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2803-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="b2803-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b2803-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2803-122"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2803-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2803-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2803-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2803-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b2803-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2803-125">**IMFMediaEngineClassFactory：： CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b2803-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




