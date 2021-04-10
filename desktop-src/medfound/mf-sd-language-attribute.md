---
description: 指定資料流程的語言。
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: 'MF_SD_LANGUAGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194284"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="7ca5e-103">MF \_ SD \_ LANGUAGE 屬性</span><span class="sxs-lookup"><span data-stu-id="7ca5e-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="7ca5e-104">指定資料流程的語言。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="7ca5e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7ca5e-105">Data type</span></span>

<span data-ttu-id="7ca5e-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="7ca5e-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca5e-107">備註</span><span class="sxs-lookup"><span data-stu-id="7ca5e-107">Remarks</span></span>

<span data-ttu-id="7ca5e-108">這個屬性的值是符合 RFC 1766 規範的語言標記。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="7ca5e-109">這個屬性會套用至資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="7ca5e-110">如果資料流程具有指定的語言，則媒體來源 (或任何建立資料流程描述項的物件) 可以設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="7ca5e-111">應用程式可以查詢此屬性來取得語言。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="7ca5e-112">如果未設定屬性，則資料流程沒有指定的語言。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="7ca5e-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7ca5e-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca5e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ca5e-114">Requirements</span></span>



| <span data-ttu-id="7ca5e-115">需求</span><span class="sxs-lookup"><span data-stu-id="7ca5e-115">Requirement</span></span> | <span data-ttu-id="7ca5e-116">值</span><span class="sxs-lookup"><span data-stu-id="7ca5e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca5e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ca5e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca5e-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ca5e-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7ca5e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ca5e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca5e-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ca5e-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7ca5e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7ca5e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ca5e-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ca5e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca5e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ca5e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca5e-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7ca5e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7ca5e-125">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="7ca5e-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="7ca5e-126">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="7ca5e-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="7ca5e-127">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7ca5e-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="7ca5e-128">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="7ca5e-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




