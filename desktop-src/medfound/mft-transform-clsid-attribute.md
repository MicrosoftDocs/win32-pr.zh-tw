---
description: 包含 (MFT) 之媒體基礎轉換 (CLSID) 的類別識別碼。
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: 'MFT_TRANSFORM_CLSID_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943733"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="a03bb-103">MFT \_ 轉換 \_ CLSID \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="a03bb-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="a03bb-104">包含 (MFT) 之媒體基礎轉換 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="a03bb-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="a03bb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a03bb-105">Data type</span></span>

<span data-ttu-id="a03bb-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a03bb-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="a03bb-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="a03bb-107">Get/set</span></span>

<span data-ttu-id="a03bb-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。</span><span class="sxs-lookup"><span data-stu-id="a03bb-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="a03bb-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。</span><span class="sxs-lookup"><span data-stu-id="a03bb-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="a03bb-110">備註</span><span class="sxs-lookup"><span data-stu-id="a03bb-110">Remarks</span></span>

<span data-ttu-id="a03bb-111">這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。</span><span class="sxs-lookup"><span data-stu-id="a03bb-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="a03bb-112">這個屬性會在建立 MFT 時由啟用物件在內部使用。</span><span class="sxs-lookup"><span data-stu-id="a03bb-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="a03bb-113">應用程式不應直接使用此 CLSID 來建立 MFT，因為啟用物件可能需要初始化 MFT。</span><span class="sxs-lookup"><span data-stu-id="a03bb-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="a03bb-114">因此，若要建立此 MFT 的實例，請在啟用物件上呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 。</span><span class="sxs-lookup"><span data-stu-id="a03bb-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="a03bb-115">請注意， [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函式的行為與此方面的 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函式不同。</span><span class="sxs-lookup"><span data-stu-id="a03bb-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="a03bb-116">**MFTEnum** 函式會傳回 clsid，讓應用程式傳遞至 **CoCreateInstance** 函數。</span><span class="sxs-lookup"><span data-stu-id="a03bb-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="a03bb-117">**MFTEnumEx** 函式會傳回啟用物件而非 clsid。</span><span class="sxs-lookup"><span data-stu-id="a03bb-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="a03bb-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a03bb-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a03bb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a03bb-119">Requirements</span></span>



| <span data-ttu-id="a03bb-120">需求</span><span class="sxs-lookup"><span data-stu-id="a03bb-120">Requirement</span></span> | <span data-ttu-id="a03bb-121">值</span><span class="sxs-lookup"><span data-stu-id="a03bb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a03bb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a03bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a03bb-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a03bb-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a03bb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a03bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a03bb-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a03bb-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a03bb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a03bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a03bb-127"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="a03bb-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a03bb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a03bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a03bb-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a03bb-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a03bb-130">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="a03bb-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




