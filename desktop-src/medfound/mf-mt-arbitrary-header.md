---
description: 使用 Advanced Systems 格式之二進位資料流程的特定類型資料 (ASF) 檔。
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: 'MF_MT_ARBITRARY_HEADER 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026443"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="9a1b2-103">MF \_ MT \_ 任意 \_ 標頭屬性</span><span class="sxs-lookup"><span data-stu-id="9a1b2-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="9a1b2-104">使用 Advanced Systems 格式之二進位資料流程的特定類型資料 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a1b2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9a1b2-105">Data type</span></span>

<span data-ttu-id="9a1b2-106">**[**MT \_任意 \_**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** 儲存為 **位元組 \[ \]** 的標頭</span><span class="sxs-lookup"><span data-stu-id="9a1b2-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="9a1b2-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="9a1b2-107">Get/set</span></span>

<span data-ttu-id="9a1b2-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="9a1b2-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a1b2-110">備註</span><span class="sxs-lookup"><span data-stu-id="9a1b2-110">Remarks</span></span>

<span data-ttu-id="9a1b2-111">ASF 檔案可以包含具有二進位資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="9a1b2-112">\_ \_ 媒體類型中的 MF MT 任意 \_ 標頭屬性包含描述資料流程的 [**MT \_ 任意 \_ 標頭**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)結構。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="9a1b2-113">除了 MF \_ MT \_ 任意 \_ 標頭屬性之外，ASF 二進位資料流程的媒體類型還包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="9a1b2-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="9a1b2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="9a1b2-114">Attribute</span></span>                                                 | <span data-ttu-id="9a1b2-115">描述</span><span class="sxs-lookup"><span data-stu-id="9a1b2-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="9a1b2-116">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="9a1b2-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="9a1b2-117">屬性的值為 **MFMediaType \_ Binary**。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="9a1b2-118">MF \_ MT \_ 任意 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="9a1b2-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="9a1b2-119">包含其他格式資料。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="9a1b2-120">在 Windows Media 格式 SDK 中，二進位資料流程稱為 *任意資料流程* 或 *任意* 資料流程。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="9a1b2-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9a1b2-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a1b2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a1b2-122">Requirements</span></span>



| <span data-ttu-id="9a1b2-123">需求</span><span class="sxs-lookup"><span data-stu-id="9a1b2-123">Requirement</span></span> | <span data-ttu-id="9a1b2-124">值</span><span class="sxs-lookup"><span data-stu-id="9a1b2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a1b2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a1b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a1b2-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a1b2-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a1b2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a1b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a1b2-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a1b2-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9a1b2-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9a1b2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a1b2-130"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a1b2-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a1b2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a1b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1b2-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9a1b2-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a1b2-133">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="9a1b2-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




