---
description: 包含媒體引擎的回呼介面指標。
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: 'MF_MEDIA_ENGINE_CALLBACK 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981927"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="d3e2a-103">MF \_ 媒體 \_ 引擎 \_ 回呼屬性</span><span class="sxs-lookup"><span data-stu-id="d3e2a-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="d3e2a-104">包含媒體引擎的回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="d3e2a-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="d3e2a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d3e2a-105">Data type</span></span>

<span data-ttu-id="d3e2a-106">**IMFMediaEngineNotify \* *_ 儲存為 _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="d3e2a-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="d3e2a-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="d3e2a-107">Get/set</span></span>

<span data-ttu-id="d3e2a-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="d3e2a-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="d3e2a-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="d3e2a-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e2a-110">備註</span><span class="sxs-lookup"><span data-stu-id="d3e2a-110">Remarks</span></span>

<span data-ttu-id="d3e2a-111">這個屬性的值是 [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) 介面的指標，該介面是由應用程式所執行。</span><span class="sxs-lookup"><span data-stu-id="d3e2a-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="d3e2a-112">這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。</span><span class="sxs-lookup"><span data-stu-id="d3e2a-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="d3e2a-113">屬性為必要項。</span><span class="sxs-lookup"><span data-stu-id="d3e2a-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e2a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3e2a-114">Requirements</span></span>



| <span data-ttu-id="d3e2a-115">需求</span><span class="sxs-lookup"><span data-stu-id="d3e2a-115">Requirement</span></span> | <span data-ttu-id="d3e2a-116">值</span><span class="sxs-lookup"><span data-stu-id="d3e2a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e2a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3e2a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e2a-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3e2a-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="d3e2a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3e2a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e2a-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3e2a-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="d3e2a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d3e2a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e2a-122"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e2a-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e2a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3e2a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e2a-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d3e2a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d3e2a-125">**IMFMediaEngineClassFactory：： CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d3e2a-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="d3e2a-126">**IMFMediaEngineNotify**</span><span class="sxs-lookup"><span data-stu-id="d3e2a-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




