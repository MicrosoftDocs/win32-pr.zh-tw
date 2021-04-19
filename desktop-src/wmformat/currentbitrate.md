---
title: CurrentBitrate
description: CurrentBitrate 屬性包含檔案中使用中資料流程目前的總位元速率。
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate windows Media 格式
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968878"
---
# <a name="currentbitrate"></a><span data-ttu-id="37803-104">CurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="37803-104">CurrentBitrate</span></span>

<span data-ttu-id="37803-105">CurrentBitrate 屬性包含檔案中使用中資料流程目前的總位元速率。</span><span class="sxs-lookup"><span data-stu-id="37803-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="37803-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="37803-106">Global Constant</span></span>

<span data-ttu-id="37803-107">g \_ wszWMCurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="37803-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="37803-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="37803-108">Data Type</span></span>

<span data-ttu-id="37803-109">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="37803-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="37803-110">備註</span><span class="sxs-lookup"><span data-stu-id="37803-110">Remarks</span></span>

<span data-ttu-id="37803-111">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="37803-111">This is a coded attribute.</span></span>

<span data-ttu-id="37803-112">針對 **CurrentBitrate** 抓取的值會根據所使用的物件而有所不同。</span><span class="sxs-lookup"><span data-stu-id="37803-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="37803-113">在 [讀取器] 或 [同步讀取器] 物件中，值是呼叫時的實際位元速率。</span><span class="sxs-lookup"><span data-stu-id="37803-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="37803-114">在 [中繼資料編輯器] 物件中，值是檔案的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="37803-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="37803-115">檔案的實際位元速率等於所有使用中資料流程的位元速率，加上一些額外負荷。</span><span class="sxs-lookup"><span data-stu-id="37803-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="37803-116">例如，以 Windows Media Player 播放檔案時，就會顯示這個值。</span><span class="sxs-lookup"><span data-stu-id="37803-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="37803-117">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="37803-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="37803-118">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="37803-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="37803-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37803-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37803-120">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="37803-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




