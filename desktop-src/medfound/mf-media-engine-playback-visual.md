---
description: 將 Microsoft DirectComposition 視覺效果設定為媒體引擎的播放區域。
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: 'MF_MEDIA_ENGINE_PLAYBACK_VISUAL 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e9c7366bd0fbf4bf36523cf7a68f2d6da70bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107000524"
---
# <a name="mf_media_engine_playback_visual-attribute"></a><span data-ttu-id="ac692-103">MF \_ 媒體 \_ 引擎 \_ 播放 \_ 視覺化屬性</span><span class="sxs-lookup"><span data-stu-id="ac692-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_VISUAL attribute</span></span>

<span data-ttu-id="ac692-104">將 Microsoft DirectComposition 視覺效果設定為媒體引擎的播放區域。</span><span class="sxs-lookup"><span data-stu-id="ac692-104">Sets a Microsoft DirectComposition visual as the playback region for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac692-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ac692-105">Data type</span></span>

<span data-ttu-id="ac692-106">**IDCompositionVisual \* *_ 儲存為 _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="ac692-106">**IDCompositionVisual\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="ac692-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="ac692-107">Get/set</span></span>

<span data-ttu-id="ac692-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="ac692-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="ac692-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="ac692-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac692-110">備註</span><span class="sxs-lookup"><span data-stu-id="ac692-110">Remarks</span></span>

<span data-ttu-id="ac692-111">如需 DirectComposition 的詳細資訊，請參閱 [DirectComposition](../directcomp/directcomposition-portal.md) 和 [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)。</span><span class="sxs-lookup"><span data-stu-id="ac692-111">For more information on DirectComposition, see [DirectComposition](../directcomp/directcomposition-portal.md) and [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).</span></span>

<span data-ttu-id="ac692-112">這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。</span><span class="sxs-lookup"><span data-stu-id="ac692-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac692-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac692-113">Requirements</span></span>



| <span data-ttu-id="ac692-114">需求</span><span class="sxs-lookup"><span data-stu-id="ac692-114">Requirement</span></span> | <span data-ttu-id="ac692-115">值</span><span class="sxs-lookup"><span data-stu-id="ac692-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac692-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac692-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac692-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac692-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="ac692-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac692-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac692-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac692-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ac692-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ac692-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac692-121"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac692-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac692-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac692-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac692-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ac692-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
