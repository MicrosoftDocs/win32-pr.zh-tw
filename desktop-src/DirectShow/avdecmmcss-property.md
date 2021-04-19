---
description: 指定解碼執行緒的多媒體類別排程器服務 (MMCSS) 類別。
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: 'AVDecMmcss 屬性 (Uuid .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984851"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="9504e-103">AVDecMmcss 屬性</span><span class="sxs-lookup"><span data-stu-id="9504e-103">AVDecMmcss property</span></span>

<span data-ttu-id="9504e-104">指定解碼執行緒的多媒體類別排程器服務 (MMCSS) 類別。</span><span class="sxs-lookup"><span data-stu-id="9504e-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="9504e-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9504e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9504e-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="9504e-106">Data type</span></span>

<span data-ttu-id="9504e-107">**BSTR** (**VT \_ bstr**) </span><span class="sxs-lookup"><span data-stu-id="9504e-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9504e-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="9504e-108">Property GUID</span></span>

<span data-ttu-id="9504e-109">**CODECAPI \_ AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="9504e-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="9504e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9504e-110">Property value</span></span>

<span data-ttu-id="9504e-111">這個屬性的值是 MMCSS 類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9504e-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="9504e-112">備註</span><span class="sxs-lookup"><span data-stu-id="9504e-112">Remarks</span></span>

<span data-ttu-id="9504e-113">MMCSS 可讓應用程式確保時間緊迫的處理已優先存取 CPU 資源。</span><span class="sxs-lookup"><span data-stu-id="9504e-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="9504e-114">其運作方式是將已註冊的執行緒提升為較高的執行緒優先順序，同時定期降低其優先順序，以產生時間給其他進程。</span><span class="sxs-lookup"><span data-stu-id="9504e-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="9504e-115">音訊解碼器的建議值為「音訊」，而影片解碼器的建議值為「播放」。</span><span class="sxs-lookup"><span data-stu-id="9504e-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="9504e-116">如果 MMCSS 服務無法使用，或指定的 MMCSS 類別不存在，則設定屬性不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9504e-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="9504e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9504e-117">Requirements</span></span>



| <span data-ttu-id="9504e-118">需求</span><span class="sxs-lookup"><span data-stu-id="9504e-118">Requirement</span></span> | <span data-ttu-id="9504e-119">值</span><span class="sxs-lookup"><span data-stu-id="9504e-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9504e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9504e-120">Header</span></span><br/> | <dl> <span data-ttu-id="9504e-121"><dt>Uuid。h</dt></span><span class="sxs-lookup"><span data-stu-id="9504e-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9504e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9504e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9504e-123">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="9504e-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9504e-124">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="9504e-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




