---
description: 指定最大位元速率，以位/秒為單位。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: 'AVEncCommonMaxBitRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03844935e909591b2fe3c7244db79e77e7936f1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846671"
---
# <a name="avenccommonmaxbitrate-property"></a><span data-ttu-id="faa94-104">AVEncCommonMaxBitRate 屬性</span><span class="sxs-lookup"><span data-stu-id="faa94-104">AVEncCommonMaxBitRate property</span></span>

<span data-ttu-id="faa94-105">指定最大位元速率，以位/秒為單位。</span><span class="sxs-lookup"><span data-stu-id="faa94-105">Specifies the maximum bit rate, in bits per second.</span></span> <span data-ttu-id="faa94-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="faa94-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="faa94-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="faa94-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="faa94-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="faa94-108">Data type</span></span>

<span data-ttu-id="faa94-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="faa94-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="faa94-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="faa94-110">Property GUID</span></span>

<span data-ttu-id="faa94-111">**CODECAPI \_ AVEncCommonMaxBitRate**</span><span class="sxs-lookup"><span data-stu-id="faa94-111">**CODECAPI\_AVEncCommonMaxBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="faa94-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="faa94-112">Property value</span></span>

<span data-ttu-id="faa94-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="faa94-113">This property has a linear range of values.</span></span> <span data-ttu-id="faa94-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="faa94-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="faa94-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="faa94-115">Requirements</span></span>



| <span data-ttu-id="faa94-116">需求</span><span class="sxs-lookup"><span data-stu-id="faa94-116">Requirement</span></span> | <span data-ttu-id="faa94-117">值</span><span class="sxs-lookup"><span data-stu-id="faa94-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="faa94-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="faa94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="faa94-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="faa94-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="faa94-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="faa94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="faa94-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="faa94-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="faa94-122">標頭</span><span class="sxs-lookup"><span data-stu-id="faa94-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa94-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="faa94-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa94-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faa94-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa94-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="faa94-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="faa94-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="faa94-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




