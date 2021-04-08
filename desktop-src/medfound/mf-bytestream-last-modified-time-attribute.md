---
description: 指定上一次修改位元組資料流程的時間。
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: 'MF_BYTESTREAM_LAST_MODIFIED_TIME 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691819"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="cd863-103">MF \_ BYTESTREAM \_ 上次 \_ 修改 \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="cd863-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="cd863-104">指定上一次修改位元組資料流程的時間。</span><span class="sxs-lookup"><span data-stu-id="cd863-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="cd863-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cd863-105">Data type</span></span>

<span data-ttu-id="cd863-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="cd863-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="cd863-107">備註</span><span class="sxs-lookup"><span data-stu-id="cd863-107">Remarks</span></span>

<span data-ttu-id="cd863-108">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="cd863-108">This attribute is optional.</span></span> <span data-ttu-id="cd863-109">屬性的值是 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構。</span><span class="sxs-lookup"><span data-stu-id="cd863-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="cd863-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="cd863-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd863-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd863-111">Requirements</span></span>



| <span data-ttu-id="cd863-112">需求</span><span class="sxs-lookup"><span data-stu-id="cd863-112">Requirement</span></span> | <span data-ttu-id="cd863-113">值</span><span class="sxs-lookup"><span data-stu-id="cd863-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd863-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd863-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cd863-115">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd863-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="cd863-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd863-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cd863-117">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd863-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="cd863-118">標頭</span><span class="sxs-lookup"><span data-stu-id="cd863-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd863-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="cd863-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd863-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd863-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd863-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="cd863-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cd863-122">位元組資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="cd863-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="cd863-123">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="cd863-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="cd863-124">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="cd863-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="cd863-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="cd863-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
