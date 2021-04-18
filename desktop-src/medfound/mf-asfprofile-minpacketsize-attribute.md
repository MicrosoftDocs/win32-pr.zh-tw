---
description: 指定 ASF 檔案的最小封包大小（以位元組為單位）。
ms.assetid: 22e5725d-de55-4a0c-a6cc-1ed9f20e7663
title: 'MF_ASFPROFILE_MINPACKETSIZE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8e1aaea4fe1dfc2c6e01e969bc8b588ac21e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971484"
---
# <a name="mf_asfprofile_minpacketsize-attribute"></a><span data-ttu-id="7e3ca-103">MF \_ ASFPROFILE \_ MINPACKETSIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="7e3ca-103">MF\_ASFPROFILE\_MINPACKETSIZE attribute</span></span>

<span data-ttu-id="7e3ca-104">指定 ASF 檔案的最小封包大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-104">Specifies the minimum packet size for an ASF file, in bytes.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e3ca-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7e3ca-105">Data type</span></span>

<span data-ttu-id="7e3ca-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7e3ca-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e3ca-107">備註</span><span class="sxs-lookup"><span data-stu-id="7e3ca-107">Remarks</span></span>

<span data-ttu-id="7e3ca-108">這個屬性會套用至 ASF 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-108">This attribute applies to ASF profile objects.</span></span> <span data-ttu-id="7e3ca-109">若要設定這個屬性，請使用 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-109">To set this attribute, use the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>

<span data-ttu-id="7e3ca-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7e3ca-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e3ca-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e3ca-111">Requirements</span></span>



| <span data-ttu-id="7e3ca-112">需求</span><span class="sxs-lookup"><span data-stu-id="7e3ca-112">Requirement</span></span> | <span data-ttu-id="7e3ca-113">值</span><span class="sxs-lookup"><span data-stu-id="7e3ca-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e3ca-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e3ca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7e3ca-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e3ca-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7e3ca-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e3ca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7e3ca-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e3ca-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7e3ca-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7e3ca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e3ca-119"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e3ca-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e3ca-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e3ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e3ca-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7e3ca-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e3ca-122">ASF 屬性</span><span class="sxs-lookup"><span data-stu-id="7e3ca-122">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e3ca-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7e3ca-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7e3ca-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7e3ca-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




