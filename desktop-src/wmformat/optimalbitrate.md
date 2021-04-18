---
title: OptimalBitrate
description: OptimalBitrate 屬性包含最佳播放檔案的位元速率。
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate windows Media 格式
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968469"
---
# <a name="optimalbitrate"></a><span data-ttu-id="c26d0-104">OptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="c26d0-104">OptimalBitrate</span></span>

<span data-ttu-id="c26d0-105">**OptimalBitrate** 屬性包含最佳播放檔案的位元速率。</span><span class="sxs-lookup"><span data-stu-id="c26d0-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c26d0-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="c26d0-106">Global Constant</span></span>

<span data-ttu-id="c26d0-107">g \_ wszWMOptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="c26d0-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="c26d0-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="c26d0-108">Data Type</span></span>

<span data-ttu-id="c26d0-109">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c26d0-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c26d0-110">備註</span><span class="sxs-lookup"><span data-stu-id="c26d0-110">Remarks</span></span>

<span data-ttu-id="c26d0-111">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="c26d0-111">This is a coded attribute.</span></span>

<span data-ttu-id="c26d0-112">針對包含變數位元速率 (VBR) 資料流程的檔案，這個值是檔案中資料流程的尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="c26d0-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="c26d0-113">針對沒有 VBR 的檔案，此值與 [**位元速率**](bit-rate.md)相同。</span><span class="sxs-lookup"><span data-stu-id="c26d0-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="c26d0-114">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="c26d0-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="c26d0-115">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="c26d0-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="c26d0-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c26d0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c26d0-117">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="c26d0-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




