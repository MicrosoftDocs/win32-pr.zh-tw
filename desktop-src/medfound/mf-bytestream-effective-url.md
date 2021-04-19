---
description: 取得位元組資料流程的有效 URL。
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: 'MF_BYTESTREAM_EFFECTIVE_URL 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981429"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="12db6-103">MF \_ BYTESTREAM \_ 有效 \_ URL 屬性</span><span class="sxs-lookup"><span data-stu-id="12db6-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="12db6-104">取得位元組資料流程的有效 URL。</span><span class="sxs-lookup"><span data-stu-id="12db6-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="12db6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="12db6-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="12db6-106">取得/設定</span><span class="sxs-lookup"><span data-stu-id="12db6-106">Get/set</span></span>

<span data-ttu-id="12db6-107">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="12db6-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="12db6-108">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="12db6-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="12db6-109">適用於</span><span class="sxs-lookup"><span data-stu-id="12db6-109">Applies to</span></span>

[<span data-ttu-id="12db6-110">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="12db6-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="12db6-111">備註</span><span class="sxs-lookup"><span data-stu-id="12db6-111">Remarks</span></span>

<span data-ttu-id="12db6-112">如果原始 URL 包含任何額外的資訊（例如搜尋字串或錨點），或如果已重新導向要求，有效的 URL 可能會與原始的 url 不同。</span><span class="sxs-lookup"><span data-stu-id="12db6-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="12db6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="12db6-113">Requirements</span></span>



| <span data-ttu-id="12db6-114">需求</span><span class="sxs-lookup"><span data-stu-id="12db6-114">Requirement</span></span> | <span data-ttu-id="12db6-115">值</span><span class="sxs-lookup"><span data-stu-id="12db6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12db6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12db6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12db6-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12db6-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="12db6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12db6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12db6-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12db6-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="12db6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="12db6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12db6-121"><dt>Mfobjects。h</dt></span><span class="sxs-lookup"><span data-stu-id="12db6-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12db6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12db6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12db6-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="12db6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="12db6-124">位元組資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="12db6-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="12db6-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="12db6-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




