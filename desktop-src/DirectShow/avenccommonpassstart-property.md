---
description: 啟動第一次編碼傳遞。
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: 'AVEncCommonPassStart 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d5be37fc4866aea6f442d4d8a2c0f74c6609cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385795"
---
# <a name="avenccommonpassstart-property"></a><span data-ttu-id="282ae-103">AVEncCommonPassStart 屬性</span><span class="sxs-lookup"><span data-stu-id="282ae-103">AVEncCommonPassStart property</span></span>

<span data-ttu-id="282ae-104">啟動第一次編碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="282ae-104">Starts the first encoding pass.</span></span>

<span data-ttu-id="282ae-105">此屬性是唯寫的。</span><span class="sxs-lookup"><span data-stu-id="282ae-105">This property is write-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="282ae-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="282ae-106">Data type</span></span>

<span data-ttu-id="282ae-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="282ae-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="282ae-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="282ae-108">Property GUID</span></span>

<span data-ttu-id="282ae-109">**CODECAPI \_ AVEncCommonPassStart**</span><span class="sxs-lookup"><span data-stu-id="282ae-109">**CODECAPI\_AVEncCommonPassStart**</span></span>

## <a name="property-value"></a><span data-ttu-id="282ae-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="282ae-110">Property value</span></span>

<span data-ttu-id="282ae-111">這個屬性的值是要開始的編碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="282ae-111">The value of this property is the encoding pass to start.</span></span> <span data-ttu-id="282ae-112">若要取得支援值的範圍，請查詢編碼器的 [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="282ae-112">To get the range of supported values, query the encoder's [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="282ae-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="282ae-113">Requirements</span></span>



| <span data-ttu-id="282ae-114">需求</span><span class="sxs-lookup"><span data-stu-id="282ae-114">Requirement</span></span> | <span data-ttu-id="282ae-115">值</span><span class="sxs-lookup"><span data-stu-id="282ae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="282ae-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="282ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="282ae-117">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="282ae-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="282ae-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="282ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="282ae-119">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="282ae-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="282ae-120">標頭</span><span class="sxs-lookup"><span data-stu-id="282ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="282ae-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="282ae-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="282ae-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="282ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="282ae-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="282ae-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="282ae-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="282ae-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




