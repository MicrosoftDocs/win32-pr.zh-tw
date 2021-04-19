---
description: 指定媒體基礎轉換 (MFT) 是否支援動態格式變更。
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: 'MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996669"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="8d5df-103">MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更屬性</span><span class="sxs-lookup"><span data-stu-id="8d5df-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="8d5df-104">指定媒體基礎轉換 (MFT) 是否支援動態格式變更。</span><span class="sxs-lookup"><span data-stu-id="8d5df-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="8d5df-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8d5df-105">Data type</span></span>

<span data-ttu-id="8d5df-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8d5df-106">**UINT32**</span></span>

<span data-ttu-id="8d5df-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="8d5df-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5df-108">備註</span><span class="sxs-lookup"><span data-stu-id="8d5df-108">Remarks</span></span>

<span data-ttu-id="8d5df-109">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="8d5df-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="8d5df-110">值</span><span class="sxs-lookup"><span data-stu-id="8d5df-110">Value</span></span>     | <span data-ttu-id="8d5df-111">描述</span><span class="sxs-lookup"><span data-stu-id="8d5df-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="8d5df-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="8d5df-112">**TRUE**</span></span>  | <span data-ttu-id="8d5df-113">用戶端可以在串流期間變更輸入格式。</span><span class="sxs-lookup"><span data-stu-id="8d5df-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="8d5df-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="8d5df-114">**FALSE**</span></span> | <span data-ttu-id="8d5df-115">必須先清空 MFT，用戶端才能變更輸入格式。</span><span class="sxs-lookup"><span data-stu-id="8d5df-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="8d5df-116">若要取得這個屬性，請先呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="8d5df-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="8d5df-117">然後呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="8d5df-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="8d5df-118">如果 [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 失敗或屬性不存在，則預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8d5df-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="8d5df-119">[非同步 MFTs](asynchronous-mfts.md) 必須傳回 **TRUE** 值。</span><span class="sxs-lookup"><span data-stu-id="8d5df-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="8d5df-120">如需詳細資訊，請參閱 [處理資料流程變更](handling-stream-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="8d5df-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="8d5df-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="8d5df-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5df-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d5df-122">Requirements</span></span>



| <span data-ttu-id="8d5df-123">需求</span><span class="sxs-lookup"><span data-stu-id="8d5df-123">Requirement</span></span> | <span data-ttu-id="8d5df-124">值</span><span class="sxs-lookup"><span data-stu-id="8d5df-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5df-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d5df-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5df-126">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d5df-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8d5df-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d5df-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5df-128">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d5df-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8d5df-129">標頭</span><span class="sxs-lookup"><span data-stu-id="8d5df-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d5df-130"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d5df-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5df-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d5df-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5df-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8d5df-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8d5df-133">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="8d5df-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="8d5df-134">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="8d5df-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="8d5df-135">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8d5df-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8d5df-136">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8d5df-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8d5df-137">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8d5df-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




