---
description: 包含媒體基礎轉換 (MFT) 的已註冊輸入類型。
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: 'MFT_INPUT_TYPES_Attributes 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512605"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="e834f-103">MFT \_ 輸入 \_ 類型 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="e834f-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="e834f-104">包含媒體基礎轉換 (MFT) 的已註冊輸入類型。</span><span class="sxs-lookup"><span data-stu-id="e834f-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="e834f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e834f-105">Data type</span></span>

<span data-ttu-id="e834f-106">**MFT \_儲存 \_ 為 \_ \[ \]** **位元組 \[ 的註冊類型 \]** 資訊</span><span class="sxs-lookup"><span data-stu-id="e834f-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="e834f-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e834f-107">Get/set</span></span>

<span data-ttu-id="e834f-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="e834f-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="e834f-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="e834f-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="e834f-110">備註</span><span class="sxs-lookup"><span data-stu-id="e834f-110">Remarks</span></span>

<span data-ttu-id="e834f-111">這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。</span><span class="sxs-lookup"><span data-stu-id="e834f-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="e834f-112">此屬性包含 [**mft 登錄 \_ \_ 類型 \_ 資訊**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) 結構的陣列，其描述 mft 所支援的一或多個輸入格式。</span><span class="sxs-lookup"><span data-stu-id="e834f-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="e834f-113">這些值會從登錄中取得，並作為應用程式的提示。</span><span class="sxs-lookup"><span data-stu-id="e834f-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="e834f-114">MFT 可能會支援其他格式。</span><span class="sxs-lookup"><span data-stu-id="e834f-114">The MFT might support additional formats.</span></span> <span data-ttu-id="e834f-115">若要設定實際的輸入格式，您必須建立 MFT 並呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)。</span><span class="sxs-lookup"><span data-stu-id="e834f-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="e834f-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e834f-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e834f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e834f-117">Requirements</span></span>



| <span data-ttu-id="e834f-118">需求</span><span class="sxs-lookup"><span data-stu-id="e834f-118">Requirement</span></span> | <span data-ttu-id="e834f-119">值</span><span class="sxs-lookup"><span data-stu-id="e834f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e834f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e834f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e834f-121">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e834f-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e834f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e834f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e834f-123">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e834f-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e834f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e834f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e834f-125"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="e834f-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e834f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e834f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e834f-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e834f-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e834f-128">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="e834f-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




