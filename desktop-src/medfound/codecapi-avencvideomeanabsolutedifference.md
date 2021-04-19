---
description: 控制 \_ 每個輸出範例上的 MFSampleExtension MeanAbsoluteDifference 透過 IMFAttribute 的信號。
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: 'CODECAPI_AVEncVideoMeanAbsoluteDifference 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986281"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="91516-103">CODECAPI \_ AVEncVideoMeanAbsoluteDifference 屬性</span><span class="sxs-lookup"><span data-stu-id="91516-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="91516-104">控制每個輸出範例上的 [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) 透過 [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 的信號。</span><span class="sxs-lookup"><span data-stu-id="91516-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="91516-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="91516-105">Data type</span></span>

<span data-ttu-id="91516-106">**ULONG** (VT \_ UI4) </span><span class="sxs-lookup"><span data-stu-id="91516-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="91516-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="91516-107">Property GUID</span></span>

<span data-ttu-id="91516-108">**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**</span><span class="sxs-lookup"><span data-stu-id="91516-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="91516-109">備註</span><span class="sxs-lookup"><span data-stu-id="91516-109">Remarks</span></span>

<span data-ttu-id="91516-110">如果應用程式設定非零值，則編碼器應該將 [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) 範例屬性新增至每個輸出範例。</span><span class="sxs-lookup"><span data-stu-id="91516-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="91516-111">MFSampleExtension \_ MeanAbsoluteDifference 屬性會指出來源樣本與 Y 平面中預測樣本之間的平均絕對差異。</span><span class="sxs-lookup"><span data-stu-id="91516-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="91516-112">如果編碼器針對 **GetParameterRange** 傳回0，則編碼器不支援輸出範例上 [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) 的輸出。</span><span class="sxs-lookup"><span data-stu-id="91516-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="91516-113">預設值應為0。</span><span class="sxs-lookup"><span data-stu-id="91516-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="91516-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="91516-114">Requirements</span></span>



| <span data-ttu-id="91516-115">需求</span><span class="sxs-lookup"><span data-stu-id="91516-115">Requirement</span></span> | <span data-ttu-id="91516-116">值</span><span class="sxs-lookup"><span data-stu-id="91516-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91516-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91516-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91516-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91516-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="91516-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91516-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91516-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91516-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="91516-121">標頭</span><span class="sxs-lookup"><span data-stu-id="91516-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91516-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="91516-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91516-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91516-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91516-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="91516-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




