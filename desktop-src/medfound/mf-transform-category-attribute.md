---
description: 指定媒體基礎轉換 (MFT) 的分類。
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: 'MF_TRANSFORM_CATEGORY_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191621"
---
# <a name="mf_transform_category_attribute-attribute"></a><span data-ttu-id="a38ad-103">MF \_ 轉換 \_ 類別目錄 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="a38ad-103">MF\_TRANSFORM\_CATEGORY\_Attribute attribute</span></span>

<span data-ttu-id="a38ad-104">指定媒體基礎轉換 (MFT) 的分類。</span><span class="sxs-lookup"><span data-stu-id="a38ad-104">Specifies the category for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="a38ad-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a38ad-105">Data type</span></span>

<span data-ttu-id="a38ad-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a38ad-106">**GUID**</span></span>

<span data-ttu-id="a38ad-107">如需可能值的清單，請參閱 [**MFT \_ 類別目錄**](mft-category.md)。</span><span class="sxs-lookup"><span data-stu-id="a38ad-107">For a list of possible values, see [**MFT\_CATEGORY**](mft-category.md).</span></span>

## <a name="getset"></a><span data-ttu-id="a38ad-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="a38ad-108">Get/set</span></span>

<span data-ttu-id="a38ad-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。</span><span class="sxs-lookup"><span data-stu-id="a38ad-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="a38ad-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。</span><span class="sxs-lookup"><span data-stu-id="a38ad-110">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="a38ad-111">備註</span><span class="sxs-lookup"><span data-stu-id="a38ad-111">Remarks</span></span>

<span data-ttu-id="a38ad-112">這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。</span><span class="sxs-lookup"><span data-stu-id="a38ad-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38ad-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a38ad-113">Requirements</span></span>



| <span data-ttu-id="a38ad-114">需求</span><span class="sxs-lookup"><span data-stu-id="a38ad-114">Requirement</span></span> | <span data-ttu-id="a38ad-115">值</span><span class="sxs-lookup"><span data-stu-id="a38ad-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38ad-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a38ad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a38ad-117">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a38ad-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a38ad-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a38ad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a38ad-119">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a38ad-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a38ad-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a38ad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a38ad-121"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="a38ad-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38ad-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a38ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38ad-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a38ad-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a38ad-124">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="a38ad-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




