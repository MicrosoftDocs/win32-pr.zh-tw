---
description: 指定編碼器將使用的執行緒數目。
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: 'MFPKEY_NUMTHREADS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513104"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="4569b-103">MFPKEY \_ NUMTHREADS 屬性</span><span class="sxs-lookup"><span data-stu-id="4569b-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="4569b-104">指定編碼器將使用的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="4569b-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4569b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="4569b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4569b-106">g \_ wszWMVCNumThreads</span><span class="sxs-lookup"><span data-stu-id="4569b-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="4569b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4569b-107">Data Type</span></span>

<span data-ttu-id="4569b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4569b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4569b-109">預設值</span><span class="sxs-lookup"><span data-stu-id="4569b-109">Default Value</span></span>

<span data-ttu-id="4569b-110">1</span><span class="sxs-lookup"><span data-stu-id="4569b-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="4569b-111">備註</span><span class="sxs-lookup"><span data-stu-id="4569b-111">Remarks</span></span>

<span data-ttu-id="4569b-112">此值旨在將編碼劃分成多個執行緒，以利用具有多個處理器的電腦。</span><span class="sxs-lookup"><span data-stu-id="4569b-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="4569b-113">相較于單一執行緒，將編碼工作分割成多個執行緒可能會導致品質稍微降低。</span><span class="sxs-lookup"><span data-stu-id="4569b-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="4569b-114">針對 (wmvencod.dll) Windows XP 和 Windows Vista 發行的影片編碼器，這個屬性應該設定為1、2或4。</span><span class="sxs-lookup"><span data-stu-id="4569b-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="4569b-115">其他值將會四捨五入。</span><span class="sxs-lookup"><span data-stu-id="4569b-115">Other values will be rounded down.</span></span>

<span data-ttu-id="4569b-116">針對與 Windows 7 一起發行的影片編碼器 (wmvencod.dll) ，此屬性應該設定為1、2、4或8。</span><span class="sxs-lookup"><span data-stu-id="4569b-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="4569b-117">其他值將會四捨五入。</span><span class="sxs-lookup"><span data-stu-id="4569b-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="4569b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4569b-118">Requirements</span></span>



| <span data-ttu-id="4569b-119">需求</span><span class="sxs-lookup"><span data-stu-id="4569b-119">Requirement</span></span> | <span data-ttu-id="4569b-120">值</span><span class="sxs-lookup"><span data-stu-id="4569b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4569b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4569b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4569b-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4569b-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4569b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4569b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4569b-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4569b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4569b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4569b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4569b-126"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4569b-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4569b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4569b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4569b-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="4569b-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




