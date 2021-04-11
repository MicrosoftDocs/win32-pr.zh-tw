---
description: 包含媒體基礎轉換 (MFT) 啟用物件的旗標。
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: 'MF_TRANSFORM_FLAGS_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943640"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="61d10-103">MF \_ 轉換 \_ 旗標 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="61d10-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="61d10-104">包含媒體基礎轉換 (MFT) 啟用物件的旗標。</span><span class="sxs-lookup"><span data-stu-id="61d10-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="61d10-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="61d10-105">Data type</span></span>

<span data-ttu-id="61d10-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="61d10-106">**UINT32**</span></span>

<span data-ttu-id="61d10-107">值是來自 [**\_ MFT \_ 列舉 \_ 旗**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag)標列舉的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="61d10-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="61d10-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="61d10-108">Get/set</span></span>

<span data-ttu-id="61d10-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="61d10-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="61d10-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="61d10-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="61d10-111">備註</span><span class="sxs-lookup"><span data-stu-id="61d10-111">Remarks</span></span>

<span data-ttu-id="61d10-112">這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。</span><span class="sxs-lookup"><span data-stu-id="61d10-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="61d10-113">屬性包含描述 MFT 的旗標。</span><span class="sxs-lookup"><span data-stu-id="61d10-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d10-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="61d10-114">Requirements</span></span>



| <span data-ttu-id="61d10-115">需求</span><span class="sxs-lookup"><span data-stu-id="61d10-115">Requirement</span></span> | <span data-ttu-id="61d10-116">值</span><span class="sxs-lookup"><span data-stu-id="61d10-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d10-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61d10-117">Minimum supported client</span></span><br/> | <span data-ttu-id="61d10-118">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61d10-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="61d10-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61d10-119">Minimum supported server</span></span><br/> | <span data-ttu-id="61d10-120">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61d10-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="61d10-121">標頭</span><span class="sxs-lookup"><span data-stu-id="61d10-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d10-122"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="61d10-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61d10-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61d10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d10-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="61d10-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="61d10-125">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="61d10-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
