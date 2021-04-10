---
description: 指定拓撲載入器是否會變更媒體基礎轉換 (MFT) 的媒體類型。 應用程式通常不會使用此屬性。
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: 'MF_ACTI加值稅E_MFT_LOCKED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114609"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="1c931-104">MF \_ 啟動 \_ MFT \_ 鎖定屬性</span><span class="sxs-lookup"><span data-stu-id="1c931-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="1c931-105">指定拓撲載入器是否會變更媒體基礎轉換 (MFT) 的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1c931-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="1c931-106">應用程式通常不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="1c931-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c931-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1c931-107">Data type</span></span>

<span data-ttu-id="1c931-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1c931-108">**UINT32**</span></span>

<span data-ttu-id="1c931-109">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="1c931-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c931-110">備註</span><span class="sxs-lookup"><span data-stu-id="1c931-110">Remarks</span></span>

<span data-ttu-id="1c931-111">如果這個屬性的值為非零值，拓撲載入器不會變更 MFT 上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1c931-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="1c931-112">拓撲載入器會在載入拓撲之後設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="1c931-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="1c931-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="1c931-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c931-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c931-114">Requirements</span></span>



| <span data-ttu-id="1c931-115">需求</span><span class="sxs-lookup"><span data-stu-id="1c931-115">Requirement</span></span> | <span data-ttu-id="1c931-116">值</span><span class="sxs-lookup"><span data-stu-id="1c931-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c931-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c931-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c931-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c931-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c931-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c931-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c931-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c931-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c931-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1c931-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c931-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c931-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c931-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c931-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c931-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1c931-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c931-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1c931-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1c931-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1c931-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1c931-127">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="1c931-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




