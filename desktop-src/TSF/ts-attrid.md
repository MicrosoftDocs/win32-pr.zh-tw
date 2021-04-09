---
title: 'TS_ATTRID (Textstor) '
description: TS \_ ATTRID 資料類型是用來識別文字屬性。
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ea3823a95c123fe9942f69a2a133fd94a8567a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685478"
---
# <a name="ts_attrid"></a><span data-ttu-id="90b6a-104">TS \_ ATTRID</span><span class="sxs-lookup"><span data-stu-id="90b6a-104">TS\_ATTRID</span></span>

<span data-ttu-id="90b6a-105">**TS \_ ATTRID** 資料類型是用來識別文字屬性。</span><span class="sxs-lookup"><span data-stu-id="90b6a-105">The **TS\_ATTRID** data type is used to identify a text attribute.</span></span>


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a><span data-ttu-id="90b6a-106">備註</span><span class="sxs-lookup"><span data-stu-id="90b6a-106">Remarks</span></span>

<span data-ttu-id="90b6a-107">預先定義的 TS ATTRID Guid 清單 \_ 位於 tsattrs。</span><span class="sxs-lookup"><span data-stu-id="90b6a-107">A list of predefined GUIDs for TS\_ATTRID is in tsattrs.h.</span></span>

<span data-ttu-id="90b6a-108">Guid TSATTRID \_ 文字 \_ VERTICALWRITING 和 TSATTRID \_ 文字方向適用于 \_ 應用程式，以符合要更正的輸入文字。</span><span class="sxs-lookup"><span data-stu-id="90b6a-108">The GUIDs TSATTRID\_Text\_VerticalWriting and TSATTRID\_Text\_Orientation are useful for applications to match input text that is to be corrected.</span></span> <span data-ttu-id="90b6a-109">您可以建立其他使用者定義的 Guid。</span><span class="sxs-lookup"><span data-stu-id="90b6a-109">Additional user-defined GUIDs can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="90b6a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="90b6a-110">Requirements</span></span>



| <span data-ttu-id="90b6a-111">需求</span><span class="sxs-lookup"><span data-stu-id="90b6a-111">Requirement</span></span> | <span data-ttu-id="90b6a-112">值</span><span class="sxs-lookup"><span data-stu-id="90b6a-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90b6a-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90b6a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="90b6a-114">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90b6a-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="90b6a-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90b6a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="90b6a-116">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90b6a-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="90b6a-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="90b6a-117">Redistributable</span></span><br/>          | <span data-ttu-id="90b6a-118">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="90b6a-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="90b6a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="90b6a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="90b6a-120"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="90b6a-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="90b6a-121">Idl</span><span class="sxs-lookup"><span data-stu-id="90b6a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90b6a-122"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="90b6a-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90b6a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90b6a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90b6a-124">**ITextStoreACP：： FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="90b6a-124">**ITextStoreACP::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="90b6a-125">**ITextStoreACP：： RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="90b6a-125">**ITextStoreACP::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="90b6a-126">**ITextStoreACP：： RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="90b6a-126">**ITextStoreACP::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="90b6a-127">**ITextStoreACP：： RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="90b6a-127">**ITextStoreACP::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="90b6a-128">**ITextStoreACPSink：： OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="90b6a-128">**ITextStoreACPSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="90b6a-129">**ITextStoreAnchor::FindNextAttrTransition**</span><span class="sxs-lookup"><span data-stu-id="90b6a-129">**ITextStoreAnchor::FindNextAttrTransition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[<span data-ttu-id="90b6a-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span><span class="sxs-lookup"><span data-stu-id="90b6a-130">**ITextStoreAnchor::RequestAttrsAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[<span data-ttu-id="90b6a-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span><span class="sxs-lookup"><span data-stu-id="90b6a-131">**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[<span data-ttu-id="90b6a-132">**ITextStoreAnchor::RequestSupportedAttrs**</span><span class="sxs-lookup"><span data-stu-id="90b6a-132">**ITextStoreAnchor::RequestSupportedAttrs**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[<span data-ttu-id="90b6a-133">**ITextStoreAnchorSink::OnAttrsChange**</span><span class="sxs-lookup"><span data-stu-id="90b6a-133">**ITextStoreAnchorSink::OnAttrsChange**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[<span data-ttu-id="90b6a-134">**TS \_ ATTRVAL**</span><span class="sxs-lookup"><span data-stu-id="90b6a-134">**TS\_ATTRVAL**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





