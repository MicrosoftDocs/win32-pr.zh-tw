---
description: 包含針對資料流程所定義的已同步可存取媒體交換 (薩米) 語言名稱。
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: 'MF_SD_SAMI_LANGUAGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989016"
---
# <a name="mf_sd_sami_language-attribute"></a><span data-ttu-id="9ea17-103">MF \_ SD \_ 薩米文 \_ 語言屬性</span><span class="sxs-lookup"><span data-stu-id="9ea17-103">MF\_SD\_SAMI\_LANGUAGE attribute</span></span>

<span data-ttu-id="9ea17-104">包含針對資料流程所定義的已同步可存取媒體交換 (薩米) 語言名稱。</span><span class="sxs-lookup"><span data-stu-id="9ea17-104">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span>

<span data-ttu-id="9ea17-105">這個屬性會出現在從薩米文媒體來源傳回的資料流程描述項中。</span><span class="sxs-lookup"><span data-stu-id="9ea17-105">This attribute is present in the stream descriptors returned from the SAMI media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9ea17-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="9ea17-106">Data type</span></span>

<span data-ttu-id="9ea17-107">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="9ea17-107">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea17-108">備註</span><span class="sxs-lookup"><span data-stu-id="9ea17-108">Remarks</span></span>

<span data-ttu-id="9ea17-109">薩米文的語言名稱是在薩米文的檔案中指定。</span><span class="sxs-lookup"><span data-stu-id="9ea17-109">The SAMI language name is specified in the SAMI file.</span></span>

<span data-ttu-id="9ea17-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9ea17-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea17-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ea17-111">Requirements</span></span>



| <span data-ttu-id="9ea17-112">需求</span><span class="sxs-lookup"><span data-stu-id="9ea17-112">Requirement</span></span> | <span data-ttu-id="9ea17-113">值</span><span class="sxs-lookup"><span data-stu-id="9ea17-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea17-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ea17-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9ea17-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ea17-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9ea17-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ea17-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9ea17-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9ea17-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9ea17-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9ea17-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ea17-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ea17-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ea17-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ea17-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea17-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9ea17-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9ea17-122">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="9ea17-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="9ea17-123">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="9ea17-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="9ea17-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9ea17-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="9ea17-125">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="9ea17-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="9ea17-126">**IMFSAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="9ea17-126">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




