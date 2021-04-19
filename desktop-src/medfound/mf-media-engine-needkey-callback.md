---
description: 在建立時將 IMFMediaEngineNeedKeyNotify 傳遞給媒體引擎的屬性。
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993787"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="f58f5-103">MF \_ 媒體 \_ 引擎 \_ NEEDKEY \_ 回呼屬性</span><span class="sxs-lookup"><span data-stu-id="f58f5-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="f58f5-104">在建立時將 [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) 傳遞給媒體引擎的屬性。</span><span class="sxs-lookup"><span data-stu-id="f58f5-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="f58f5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f58f5-105">Data type</span></span>

<span data-ttu-id="f58f5-106">**IMFMediaEngineNeedKeyNotify \* *_ 儲存為 _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="f58f5-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="f58f5-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="f58f5-107">Get/set</span></span>

<span data-ttu-id="f58f5-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="f58f5-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="f58f5-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="f58f5-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="f58f5-110">備註</span><span class="sxs-lookup"><span data-stu-id="f58f5-110">Remarks</span></span>

<span data-ttu-id="f58f5-111">這個屬性的值是 [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) 介面的指標，該介面是由應用程式所執行。</span><span class="sxs-lookup"><span data-stu-id="f58f5-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f58f5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f58f5-112">Requirements</span></span>



| <span data-ttu-id="f58f5-113">需求</span><span class="sxs-lookup"><span data-stu-id="f58f5-113">Requirement</span></span> | <span data-ttu-id="f58f5-114">值</span><span class="sxs-lookup"><span data-stu-id="f58f5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f58f5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f58f5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f58f5-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f58f5-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f58f5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f58f5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f58f5-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f58f5-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f58f5-119">Idl</span><span class="sxs-lookup"><span data-stu-id="f58f5-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f58f5-120"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f58f5-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f58f5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f58f5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f58f5-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f58f5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




