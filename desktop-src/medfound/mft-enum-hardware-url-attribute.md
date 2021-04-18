---
description: 包含以硬體為基礎的媒體基礎轉換 (MFT) 的符號連結。
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: 'MFT_ENUM_HARDWARE_URL_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192161"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="ba327-103">MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="ba327-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="ba327-104">包含以硬體為基礎的媒體基礎轉換 (MFT) 的符號連結。</span><span class="sxs-lookup"><span data-stu-id="ba327-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="ba327-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ba327-105">Data type</span></span>

<span data-ttu-id="ba327-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ba327-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="ba327-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="ba327-107">Get/set</span></span>

<span data-ttu-id="ba327-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="ba327-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="ba327-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="ba327-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba327-110">備註</span><span class="sxs-lookup"><span data-stu-id="ba327-110">Remarks</span></span>

<span data-ttu-id="ba327-111">以硬體為基礎的 MFTs 支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ba327-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="ba327-112">屬性的值是設備磁碟機的符號連結。</span><span class="sxs-lookup"><span data-stu-id="ba327-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="ba327-113">當這些指標代表以硬體為基礎的 MFTs 時，也會在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所配置的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ba327-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="ba327-114">符號連結應該視為不透明的字串。</span><span class="sxs-lookup"><span data-stu-id="ba327-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="ba327-115">若要取得裝置的顯示名稱，請查詢 [ [MFT \_ 易記 \_ 名稱](mft-friendly-name-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba327-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="ba327-116">軟體 MFTs 不應設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ba327-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="ba327-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="ba327-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba327-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba327-118">Requirements</span></span>



| <span data-ttu-id="ba327-119">需求</span><span class="sxs-lookup"><span data-stu-id="ba327-119">Requirement</span></span> | <span data-ttu-id="ba327-120">值</span><span class="sxs-lookup"><span data-stu-id="ba327-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba327-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba327-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba327-122">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba327-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ba327-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba327-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba327-124">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba327-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ba327-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ba327-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba327-126"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba327-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba327-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba327-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba327-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ba327-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba327-129">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="ba327-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="ba327-130">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="ba327-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




