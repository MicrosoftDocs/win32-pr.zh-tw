---
title: AverageLevel
description: AverageLevel 屬性包含16位的值，用來指定音訊內容的平均音量層級。
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel windows Media 格式
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022449"
---
# <a name="averagelevel"></a><span data-ttu-id="cd929-104">AverageLevel</span><span class="sxs-lookup"><span data-stu-id="cd929-104">AverageLevel</span></span>

<span data-ttu-id="cd929-105">**AverageLevel** 屬性包含16位的值，用來指定音訊內容的平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="cd929-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="cd929-106">使用 [**PeakValue**](peakvalue.md)時，此屬性會用於正規化。</span><span class="sxs-lookup"><span data-stu-id="cd929-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="cd929-107">正規化是調整音訊檔案的播放音量層級的程式，以便在相同層級和每個檔案的平均磁片區播放 loudest 部分相同。</span><span class="sxs-lookup"><span data-stu-id="cd929-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="cd929-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="cd929-108">Global Constant</span></span>

<span data-ttu-id="cd929-109">g \_ wszAverageLevel</span><span class="sxs-lookup"><span data-stu-id="cd929-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="cd929-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="cd929-110">Data Type</span></span>

<span data-ttu-id="cd929-111">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd929-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="cd929-112">備註</span><span class="sxs-lookup"><span data-stu-id="cd929-112">Remarks</span></span>

<span data-ttu-id="cd929-113">這個屬性是由寫入器物件根據編解碼器的資訊來設定。</span><span class="sxs-lookup"><span data-stu-id="cd929-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="cd929-114">只有使用其中一個 Windows Media 音訊編解碼器壓縮的串流具有自動設定的值。</span><span class="sxs-lookup"><span data-stu-id="cd929-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="cd929-115">**AverageLevel** 不是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cd929-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="cd929-116">但是，如果 Windows Media Player 會播放檔案，您就不應該變更此值。</span><span class="sxs-lookup"><span data-stu-id="cd929-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="cd929-117">Windows Media Player 使用這個來正規化播放清單中的檔案層級。</span><span class="sxs-lookup"><span data-stu-id="cd929-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd929-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd929-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd929-119">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="cd929-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




