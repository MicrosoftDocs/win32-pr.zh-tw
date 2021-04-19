---
description: 指定位元組資料流程的原始 URL。
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: 'MF_BYTESTREAM_ORIGIN_NAME 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973672"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="e244f-103">MF \_ BYTESTREAM \_ 來源 \_ 名稱屬性</span><span class="sxs-lookup"><span data-stu-id="e244f-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="e244f-104">指定位元組資料流程的原始 URL。</span><span class="sxs-lookup"><span data-stu-id="e244f-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="e244f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e244f-105">Data type</span></span>

<span data-ttu-id="e244f-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="e244f-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="e244f-107">備註</span><span class="sxs-lookup"><span data-stu-id="e244f-107">Remarks</span></span>

<span data-ttu-id="e244f-108">以檔案為基礎的位元組資料流程可以支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="e244f-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="e244f-109">建立位元組資料流程時，會設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="e244f-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="e244f-110">若要取得屬性值，請查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的位元組資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="e244f-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="e244f-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e244f-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e244f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e244f-112">Requirements</span></span>



| <span data-ttu-id="e244f-113">需求</span><span class="sxs-lookup"><span data-stu-id="e244f-113">Requirement</span></span> | <span data-ttu-id="e244f-114">值</span><span class="sxs-lookup"><span data-stu-id="e244f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e244f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e244f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e244f-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e244f-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="e244f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e244f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e244f-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e244f-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="e244f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e244f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e244f-120"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="e244f-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e244f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e244f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e244f-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e244f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e244f-123">位元組資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="e244f-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="e244f-124">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="e244f-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="e244f-125">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="e244f-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="e244f-126">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="e244f-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




