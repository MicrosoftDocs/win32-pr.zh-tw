---
description: 包含 IMFMediaEngineExtension 介面的指標。
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: 'MF_MEDIA_ENGINE_EXTENSION 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104386326"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="60707-103">MF \_ 媒體 \_ 引擎 \_ 延伸模組屬性</span><span class="sxs-lookup"><span data-stu-id="60707-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="60707-104">包含 [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="60707-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="60707-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="60707-105">Data type</span></span>

<span data-ttu-id="60707-106">**IMFMediaEngineExtension \* *_ 儲存為 _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="60707-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="60707-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="60707-107">Get/set</span></span>

<span data-ttu-id="60707-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="60707-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="60707-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="60707-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="60707-110">備註</span><span class="sxs-lookup"><span data-stu-id="60707-110">Remarks</span></span>

<span data-ttu-id="60707-111">這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。</span><span class="sxs-lookup"><span data-stu-id="60707-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="60707-112">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="60707-112">This attribute is optional.</span></span> <span data-ttu-id="60707-113">您可以使用它來提供可實 [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="60707-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="60707-114">此介面可讓應用程式載入自訂媒體資源。</span><span class="sxs-lookup"><span data-stu-id="60707-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="60707-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="60707-115">Requirements</span></span>



| <span data-ttu-id="60707-116">需求</span><span class="sxs-lookup"><span data-stu-id="60707-116">Requirement</span></span> | <span data-ttu-id="60707-117">值</span><span class="sxs-lookup"><span data-stu-id="60707-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="60707-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60707-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60707-119">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60707-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="60707-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60707-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60707-121">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60707-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="60707-122">標頭</span><span class="sxs-lookup"><span data-stu-id="60707-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60707-123"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="60707-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60707-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60707-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60707-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="60707-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




