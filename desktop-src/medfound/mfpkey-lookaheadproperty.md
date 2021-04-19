---
description: 指定在將目前的框架編碼之前，編解碼器將評估之目前畫面格的框架數目。
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: 'MFPKEY_LOOKAHEAD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976831"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="1334b-103">MFPKEY \_ 先行屬性</span><span class="sxs-lookup"><span data-stu-id="1334b-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="1334b-104">指定在將目前的框架編碼之前，編解碼器將評估之目前畫面格的框架數目。</span><span class="sxs-lookup"><span data-stu-id="1334b-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1334b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1334b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1334b-106">g \_ wszWMVCLookAhead</span><span class="sxs-lookup"><span data-stu-id="1334b-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="1334b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1334b-107">Data Type</span></span>

<span data-ttu-id="1334b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1334b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1334b-109">預設值</span><span class="sxs-lookup"><span data-stu-id="1334b-109">Default Value</span></span>

<span data-ttu-id="1334b-110">0</span><span class="sxs-lookup"><span data-stu-id="1334b-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="1334b-111">備註</span><span class="sxs-lookup"><span data-stu-id="1334b-111">Remarks</span></span>

<span data-ttu-id="1334b-112">當編解碼器使用先行完成時，它可以更有效率地編碼影片。</span><span class="sxs-lookup"><span data-stu-id="1334b-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="1334b-113">Windows Media 格式 SDK 的寫入器物件預期編解碼器會立即編碼每個範例。</span><span class="sxs-lookup"><span data-stu-id="1334b-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="1334b-114">如此一來，這項功能在使用 writer 物件 (（包括 Windows Media 編碼器和 Windows Media Player) ）的軟體中無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1334b-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="1334b-115">與影片框架相關聯的任何資料單位延伸模組都會附加至錯誤的輸出框架。</span><span class="sxs-lookup"><span data-stu-id="1334b-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="1334b-116">資料單位擴充功能放在其中的框架數目，等於所使用的向前擴展框架數目。</span><span class="sxs-lookup"><span data-stu-id="1334b-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="1334b-117">有效的右值範圍從0到16個框架。</span><span class="sxs-lookup"><span data-stu-id="1334b-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="1334b-118">建議值為16。</span><span class="sxs-lookup"><span data-stu-id="1334b-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="1334b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1334b-119">Requirements</span></span>



| <span data-ttu-id="1334b-120">需求</span><span class="sxs-lookup"><span data-stu-id="1334b-120">Requirement</span></span> | <span data-ttu-id="1334b-121">值</span><span class="sxs-lookup"><span data-stu-id="1334b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1334b-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1334b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1334b-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1334b-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1334b-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1334b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1334b-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1334b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1334b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="1334b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1334b-127"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1334b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1334b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1334b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1334b-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1334b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




