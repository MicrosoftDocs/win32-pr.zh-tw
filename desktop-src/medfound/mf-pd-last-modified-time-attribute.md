---
description: 指定上一次修改簡報的時間。
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: 'MF_PD_LAST_MODIFIED_TIME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944587"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="3b06e-103">MF \_ PD \_ 上次 \_ 修改 \_ 時間屬性</span><span class="sxs-lookup"><span data-stu-id="3b06e-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="3b06e-104">指定上一次修改簡報的時間。</span><span class="sxs-lookup"><span data-stu-id="3b06e-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="3b06e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3b06e-105">Data type</span></span>

<span data-ttu-id="3b06e-106">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="3b06e-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="3b06e-107">備註</span><span class="sxs-lookup"><span data-stu-id="3b06e-107">Remarks</span></span>

<span data-ttu-id="3b06e-108">媒體來源可以在簡報描述項上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3b06e-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="3b06e-109">屬性的值是一個 **FILETIME** 結構，在 Windows SDK 中記載。</span><span class="sxs-lookup"><span data-stu-id="3b06e-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="3b06e-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3b06e-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b06e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b06e-111">Requirements</span></span>



| <span data-ttu-id="3b06e-112">需求</span><span class="sxs-lookup"><span data-stu-id="3b06e-112">Requirement</span></span> | <span data-ttu-id="3b06e-113">值</span><span class="sxs-lookup"><span data-stu-id="3b06e-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b06e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b06e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3b06e-115">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b06e-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="3b06e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b06e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3b06e-117">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b06e-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3b06e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3b06e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b06e-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b06e-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b06e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b06e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b06e-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3b06e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3b06e-122">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="3b06e-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="3b06e-123">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="3b06e-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="3b06e-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3b06e-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3b06e-125">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="3b06e-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




