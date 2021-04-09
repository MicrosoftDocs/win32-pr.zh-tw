---
description: 啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的音量均衡。
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: 'AVDSPLoudnessEqualization 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a2fc09077c114ab18f2626b333cfe4c87c97d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935977"
---
# <a name="avdsploudnessequalization-property"></a><span data-ttu-id="640c0-103">AVDSPLoudnessEqualization 屬性</span><span class="sxs-lookup"><span data-stu-id="640c0-103">AVDSPLoudnessEqualization property</span></span>

<span data-ttu-id="640c0-104">啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的音量均衡。</span><span class="sxs-lookup"><span data-stu-id="640c0-104">Enables or disables loudness equalization in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="640c0-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="640c0-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="640c0-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="640c0-106">Data type</span></span>

<span data-ttu-id="640c0-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="640c0-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="640c0-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="640c0-108">Property GUID</span></span>

<span data-ttu-id="640c0-109">**CODECAPI \_ AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="640c0-109">**CODECAPI\_AVDSPLoudnessEqualization**</span></span>

## <a name="property-value"></a><span data-ttu-id="640c0-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="640c0-110">Property value</span></span>

<span data-ttu-id="640c0-111">這個屬性的值是 [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="640c0-111">The value of this property is a member of the [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="640c0-112">備註</span><span class="sxs-lookup"><span data-stu-id="640c0-112">Remarks</span></span>

<span data-ttu-id="640c0-113">音量均衡是一種 DSP 程式，可在音訊串流變更時維持一致的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="640c0-113">Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="640c0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="640c0-114">Requirements</span></span>



| <span data-ttu-id="640c0-115">需求</span><span class="sxs-lookup"><span data-stu-id="640c0-115">Requirement</span></span> | <span data-ttu-id="640c0-116">值</span><span class="sxs-lookup"><span data-stu-id="640c0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="640c0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="640c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="640c0-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="640c0-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="640c0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="640c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="640c0-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="640c0-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="640c0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="640c0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="640c0-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="640c0-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640c0-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="640c0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640c0-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="640c0-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="640c0-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="640c0-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




