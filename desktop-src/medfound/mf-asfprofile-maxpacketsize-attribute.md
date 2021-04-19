---
description: 指定 ASF 檔案的封包大小上限（以位元組為單位）。
ms.assetid: c43423c2-a5f2-411c-aa47-802a3c808ad8
title: 'MF_ASFPROFILE_MAXPACKETSIZE 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5766ea3321159915b725358b365359f3efc085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974368"
---
# <a name="mf_asfprofile_maxpacketsize-attribute"></a><span data-ttu-id="9b8bf-103">MF \_ ASFPROFILE \_ MAXPACKETSIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="9b8bf-103">MF\_ASFPROFILE\_MAXPACKETSIZE attribute</span></span>

<span data-ttu-id="9b8bf-104">指定 ASF 檔案的封包大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9b8bf-104">Specifies the maximum packet size for an ASF file, in bytes.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b8bf-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9b8bf-105">Data type</span></span>

<span data-ttu-id="9b8bf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9b8bf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9b8bf-107">備註</span><span class="sxs-lookup"><span data-stu-id="9b8bf-107">Remarks</span></span>

<span data-ttu-id="9b8bf-108">這個屬性會套用至 ASF 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="9b8bf-108">This attribute applies to ASF profile objects.</span></span> <span data-ttu-id="9b8bf-109">若要設定這個屬性，請使用 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面。</span><span class="sxs-lookup"><span data-stu-id="9b8bf-109">To set this attribute, use the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>

<span data-ttu-id="9b8bf-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9b8bf-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b8bf-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b8bf-111">Requirements</span></span>



| <span data-ttu-id="9b8bf-112">需求</span><span class="sxs-lookup"><span data-stu-id="9b8bf-112">Requirement</span></span> | <span data-ttu-id="9b8bf-113">值</span><span class="sxs-lookup"><span data-stu-id="9b8bf-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8bf-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b8bf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9b8bf-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b8bf-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9b8bf-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b8bf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9b8bf-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b8bf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9b8bf-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9b8bf-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b8bf-119"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b8bf-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b8bf-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b8bf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b8bf-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9b8bf-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b8bf-122">ASF 屬性</span><span class="sxs-lookup"><span data-stu-id="9b8bf-122">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b8bf-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9b8bf-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9b8bf-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9b8bf-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




