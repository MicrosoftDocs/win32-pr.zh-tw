---
description: 指定杜比數位音訊串流中的對話方塊正規化等級（以分貝 (dB) ）。 此屬性適用于杜比數位音訊編碼器。
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: 'AVEncDDDialogNormalization 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467885"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="790c0-104">AVEncDDDialogNormalization 屬性</span><span class="sxs-lookup"><span data-stu-id="790c0-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="790c0-105">指定杜比數位音訊串流中的對話方塊正規化等級（以分貝 (dB) ）。</span><span class="sxs-lookup"><span data-stu-id="790c0-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="790c0-106">此屬性適用于杜比數位音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="790c0-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="790c0-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c0-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="790c0-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="790c0-108">Data type</span></span>

<span data-ttu-id="790c0-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="790c0-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="790c0-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="790c0-110">Property GUID</span></span>

<span data-ttu-id="790c0-111">**CODECAPI \_ AVEncDDDialogNormalization**</span><span class="sxs-lookup"><span data-stu-id="790c0-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="790c0-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="790c0-112">Property value</span></span>

<span data-ttu-id="790c0-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="790c0-113">This property has a linear range of values.</span></span> <span data-ttu-id="790c0-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="790c0-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="790c0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="790c0-115">Requirements</span></span>



| <span data-ttu-id="790c0-116">需求</span><span class="sxs-lookup"><span data-stu-id="790c0-116">Requirement</span></span> | <span data-ttu-id="790c0-117">值</span><span class="sxs-lookup"><span data-stu-id="790c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="790c0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="790c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="790c0-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790c0-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="790c0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="790c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="790c0-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790c0-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="790c0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="790c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="790c0-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="790c0-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="790c0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="790c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790c0-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="790c0-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="790c0-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="790c0-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




