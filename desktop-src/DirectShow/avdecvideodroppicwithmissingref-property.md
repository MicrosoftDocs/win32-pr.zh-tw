---
description: 指定解碼器是否在有遺漏參考框架的框架內卸載。
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: 'AVDecVideoDropPicWithMissingRef 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0c3e435ab685fca2f23fa9d0268a5e48d5387e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187453"
---
# <a name="avdecvideodroppicwithmissingref-property"></a><span data-ttu-id="4c2ac-103">AVDecVideoDropPicWithMissingRef 屬性</span><span class="sxs-lookup"><span data-stu-id="4c2ac-103">AVDecVideoDropPicWithMissingRef property</span></span>

<span data-ttu-id="4c2ac-104">指定解碼器是否在有遺漏參考框架的框架內卸載。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-104">Specifies whether the decoder drops intra frames with missing reference frames.</span></span>

<span data-ttu-id="4c2ac-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c2ac-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="4c2ac-106">Data type</span></span>

<span data-ttu-id="4c2ac-107">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="4c2ac-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4c2ac-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="4c2ac-108">Property GUID</span></span>

<span data-ttu-id="4c2ac-109">**CODECAPI \_ AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-109">**CODECAPI\_AVDecVideoDropPicWithMissingRef**</span></span>

## <a name="remarks"></a><span data-ttu-id="4c2ac-110">備註</span><span class="sxs-lookup"><span data-stu-id="4c2ac-110">Remarks</span></span>

<span data-ttu-id="4c2ac-111">如果位流損毀，框架可能會遺失參考框架。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-111">If the bitstream is corrupted, a frame might have missing reference frames.</span></span> <span data-ttu-id="4c2ac-112">如果這個屬性的值為 **VARIANT \_ TRUE**，則此解碼器會卸載框架。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-112">If the value of this property is **VARIANT\_TRUE**, the decoder drops the frame.</span></span> <span data-ttu-id="4c2ac-113">如果此值為 **VARIANT \_ FALSE**，則會嘗試使用一或多個附近的框架做為參考框架來解碼框架。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-113">If the value is **VARIANT\_FALSE**, the decoder attempts to decode the frame, using one or more nearby frames as reference frames.</span></span> <span data-ttu-id="4c2ac-114">產生的已解碼框架將會有封鎖構件。</span><span class="sxs-lookup"><span data-stu-id="4c2ac-114">The resulting decoded frame will have blocking artifacts.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c2ac-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c2ac-115">Requirements</span></span>



| <span data-ttu-id="4c2ac-116">需求</span><span class="sxs-lookup"><span data-stu-id="4c2ac-116">Requirement</span></span> | <span data-ttu-id="4c2ac-117">值</span><span class="sxs-lookup"><span data-stu-id="4c2ac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2ac-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c2ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4c2ac-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c2ac-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4c2ac-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c2ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4c2ac-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c2ac-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4c2ac-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4c2ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c2ac-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c2ac-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c2ac-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c2ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c2ac-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="4c2ac-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4c2ac-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="4c2ac-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




