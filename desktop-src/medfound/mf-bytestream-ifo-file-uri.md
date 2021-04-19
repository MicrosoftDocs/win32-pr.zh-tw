---
description: 包含 HTTP 標頭中 HTTP 伺服器所指定之 IFO (DVD 資訊) 檔案的 URL，&\# 0034;Pragma： ifoFileURI.dlna.org&\# 0034;。
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: 'MF_BYTESTREAM_IFO_FILE_URI 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975002"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="b91e6-103">MF \_ BYTESTREAM \_ IFO \_ FILE \_ URI 屬性</span><span class="sxs-lookup"><span data-stu-id="b91e6-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="b91e6-104">包含 HTTP 標頭 "Pragma： ifoFileURI.dlna.org" 中 HTTP 伺服器所指定之 IFO (DVD 資訊) 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="b91e6-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="b91e6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b91e6-105">Data type</span></span>

<span data-ttu-id="b91e6-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="b91e6-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="b91e6-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b91e6-107">Get/set</span></span>

<span data-ttu-id="b91e6-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="b91e6-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b91e6-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="b91e6-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b91e6-110">適用於</span><span class="sxs-lookup"><span data-stu-id="b91e6-110">Applies to</span></span>

[<span data-ttu-id="b91e6-111">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="b91e6-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="b91e6-112">備註</span><span class="sxs-lookup"><span data-stu-id="b91e6-112">Remarks</span></span>

<span data-ttu-id="b91e6-113">HTTP 位元組資料流程會在 HTTP 標頭中搜尋 "ifoFileURI.dlna.org" 字串。</span><span class="sxs-lookup"><span data-stu-id="b91e6-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="b91e6-114">如果找到該字串，則會將它複製到位元組資料流程上的這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b91e6-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="b91e6-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b91e6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b91e6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b91e6-116">Requirements</span></span>



| <span data-ttu-id="b91e6-117">需求</span><span class="sxs-lookup"><span data-stu-id="b91e6-117">Requirement</span></span> | <span data-ttu-id="b91e6-118">值</span><span class="sxs-lookup"><span data-stu-id="b91e6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b91e6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b91e6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b91e6-120">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b91e6-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="b91e6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b91e6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b91e6-122">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b91e6-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="b91e6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b91e6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b91e6-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="b91e6-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91e6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b91e6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91e6-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b91e6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b91e6-127">位元組資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="b91e6-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="b91e6-128">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="b91e6-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




