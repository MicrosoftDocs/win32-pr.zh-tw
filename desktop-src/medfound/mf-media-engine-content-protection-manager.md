---
description: 讓媒體引擎播放受保護的內容。
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: 'MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107000518"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="0a825-103">MF \_ 媒體 \_ 引擎 \_ 內容 \_ 保護 \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="0a825-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="0a825-104">讓媒體引擎播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="0a825-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="0a825-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0a825-105">Data type</span></span>

<span data-ttu-id="0a825-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="0a825-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="0a825-107">備註</span><span class="sxs-lookup"><span data-stu-id="0a825-107">Remarks</span></span>

<span data-ttu-id="0a825-108">這個屬性的值是 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0a825-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="0a825-109">呼叫端必須執行介面。</span><span class="sxs-lookup"><span data-stu-id="0a825-109">The caller must implement the interface.</span></span>

<span data-ttu-id="0a825-110">這個屬性可以是傳遞給 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)的其中一個屬性。</span><span class="sxs-lookup"><span data-stu-id="0a825-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="0a825-111">如果要播放受保護的內容，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="0a825-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a825-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a825-112">Requirements</span></span>



| <span data-ttu-id="0a825-113">需求</span><span class="sxs-lookup"><span data-stu-id="0a825-113">Requirement</span></span> | <span data-ttu-id="0a825-114">值</span><span class="sxs-lookup"><span data-stu-id="0a825-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a825-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a825-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0a825-116">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a825-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="0a825-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a825-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0a825-118">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a825-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="0a825-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0a825-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a825-120"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a825-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a825-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a825-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a825-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0a825-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a825-123">**IMFMediaEngineClassFactory：： CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="0a825-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




