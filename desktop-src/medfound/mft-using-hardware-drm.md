---
description: 指定 IMFTransform 是否使用硬體 DRM。
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469260"
---
# <a name="mft_using_hardware_drm-attribute"></a><span data-ttu-id="5b20b-103">\_使用 \_ 硬體 \_ DRM 屬性的 MFT</span><span class="sxs-lookup"><span data-stu-id="5b20b-103">MFT\_USING\_HARDWARE\_DRM attribute</span></span>

<span data-ttu-id="5b20b-104">指定 IMFTransform 是否使用硬體 DRM。</span><span class="sxs-lookup"><span data-stu-id="5b20b-104">Specifies whether the IMFTransform is using hardware DRM.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b20b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5b20b-105">Data type</span></span>

<span data-ttu-id="5b20b-106">**UINT32** (視為 **BOOL**) </span><span class="sxs-lookup"><span data-stu-id="5b20b-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="5b20b-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="5b20b-107">Get/set</span></span>

<span data-ttu-id="5b20b-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="5b20b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5b20b-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="5b20b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5b20b-110">適用於</span><span class="sxs-lookup"><span data-stu-id="5b20b-110">Applies to</span></span>

[<span data-ttu-id="5b20b-111">**IMTransfrom**</span><span class="sxs-lookup"><span data-stu-id="5b20b-111">**IMTransfrom**</span></span>](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a><span data-ttu-id="5b20b-112">備註</span><span class="sxs-lookup"><span data-stu-id="5b20b-112">Remarks</span></span>

<span data-ttu-id="5b20b-113">如果 MFT decrypter 指定此屬性設定為1，則會使用硬體 DRM。</span><span class="sxs-lookup"><span data-stu-id="5b20b-113">If an MFT decrypter specifies this attribute set to 1, then it is using hardware DRM.</span></span> <span data-ttu-id="5b20b-114">如果 MFT decrypter 指定此屬性設為0，則不會使用硬體 DRM。</span><span class="sxs-lookup"><span data-stu-id="5b20b-114">If an MFT decrypter specifies this attribute set to 0, then it is not using hardware DRM.</span></span> <span data-ttu-id="5b20b-115">如果 MFT decrypter 未指定此屬性，或將它指定為不同的值，則不會 (或無法) 指出它是否使用硬體 DRM。</span><span class="sxs-lookup"><span data-stu-id="5b20b-115">If an MFT decrypter does not specify this attribute or specifies it with a different value, then it does not (or is unable to) indicate whether it is using hardware DRM.</span></span>


<span data-ttu-id="5b20b-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5b20b-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b20b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b20b-117">Requirements</span></span>



| <span data-ttu-id="5b20b-118">需求</span><span class="sxs-lookup"><span data-stu-id="5b20b-118">Requirement</span></span> | <span data-ttu-id="5b20b-119">值</span><span class="sxs-lookup"><span data-stu-id="5b20b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b20b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b20b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b20b-121">Windows 10 2020 年4月更新</span><span class="sxs-lookup"><span data-stu-id="5b20b-121">Windows 10 April 2020 Update</span></span>   <br/>                                       |
| <span data-ttu-id="5b20b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b20b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b20b-123">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b20b-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5b20b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5b20b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b20b-125"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b20b-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b20b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b20b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b20b-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5b20b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="5b20b-128">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="5b20b-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




