---
description: 包含以硬體為基礎的媒體基礎轉換 (MFT) 的顯示名稱。
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: 'MFT_FRIENDLY_NAME_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982347"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="c04ec-103">MFT \_ 易記 \_ 名稱 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="c04ec-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="c04ec-104">包含以硬體為基礎的媒體基礎轉換 (MFT) 的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c04ec-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="c04ec-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c04ec-105">Data type</span></span>

<span data-ttu-id="c04ec-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c04ec-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="c04ec-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="c04ec-107">Get/set</span></span>

<span data-ttu-id="c04ec-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="c04ec-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="c04ec-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="c04ec-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="c04ec-110">備註</span><span class="sxs-lookup"><span data-stu-id="c04ec-110">Remarks</span></span>

<span data-ttu-id="c04ec-111">以硬體為基礎的 MFTs 支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="c04ec-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="c04ec-112">當這些指標代表以硬體為基礎的 MFTs 時，也會在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式所配置的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定它。</span><span class="sxs-lookup"><span data-stu-id="c04ec-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="c04ec-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c04ec-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c04ec-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c04ec-114">Requirements</span></span>



| <span data-ttu-id="c04ec-115">需求</span><span class="sxs-lookup"><span data-stu-id="c04ec-115">Requirement</span></span> | <span data-ttu-id="c04ec-116">值</span><span class="sxs-lookup"><span data-stu-id="c04ec-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c04ec-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c04ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c04ec-118">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c04ec-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c04ec-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c04ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c04ec-120">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c04ec-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c04ec-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c04ec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c04ec-122"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="c04ec-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04ec-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c04ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04ec-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c04ec-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c04ec-125">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="c04ec-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




