---
description: 指定以硬體為基礎的 Microsoft 媒體基礎的廠商識別碼。
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: MFT_ENUM_HARDWARE_VENDOR_ID_Attribute 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974115"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="b9760-103">MFT \_ 列舉 \_ 硬體 \_ 廠商 \_ 識別碼 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="b9760-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="b9760-104">指定以硬體為基礎的 Microsoft 媒體基礎轉換 (MFT) 的廠商識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9760-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="b9760-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b9760-105">Data type</span></span>

<span data-ttu-id="b9760-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b9760-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="b9760-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b9760-107">Get/set</span></span>

<span data-ttu-id="b9760-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="b9760-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b9760-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="b9760-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9760-110">備註</span><span class="sxs-lookup"><span data-stu-id="b9760-110">Remarks</span></span>

<span data-ttu-id="b9760-111">這個屬性是參考資訊，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b9760-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9760-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9760-112">Requirements</span></span>



| <span data-ttu-id="b9760-113">需求</span><span class="sxs-lookup"><span data-stu-id="b9760-113">Requirement</span></span> | <span data-ttu-id="b9760-114">值</span><span class="sxs-lookup"><span data-stu-id="b9760-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9760-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9760-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b9760-116">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9760-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="b9760-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9760-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b9760-118">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9760-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="b9760-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b9760-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9760-120"><dt>Mftransform .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9760-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9760-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9760-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9760-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b9760-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9760-123">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="b9760-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="b9760-124">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="b9760-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




