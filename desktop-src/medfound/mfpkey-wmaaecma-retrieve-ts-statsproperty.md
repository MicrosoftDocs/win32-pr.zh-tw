---
description: 指定語音捕獲 DSP 是否將時間戳記統計資料儲存在登錄中。
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: 'MFPKEY_WMAAECMA_RETRIEVE_TS_STATS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991838"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="70257-103">MFPKEY \_ WMAAECMA \_ 取得 \_ TS \_ 統計資料屬性</span><span class="sxs-lookup"><span data-stu-id="70257-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="70257-104">指定語音捕獲 DSP 是否將時間戳記統計資料儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="70257-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="70257-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="70257-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="70257-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="70257-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="70257-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="70257-107">Data Type</span></span>

<span data-ttu-id="70257-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="70257-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="70257-109">預設值</span><span class="sxs-lookup"><span data-stu-id="70257-109">Default Value</span></span>

<span data-ttu-id="70257-110">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="70257-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="70257-111">套用至</span><span class="sxs-lookup"><span data-stu-id="70257-111">Applies To</span></span>

-   [<span data-ttu-id="70257-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="70257-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="70257-113">備註</span><span class="sxs-lookup"><span data-stu-id="70257-113">Remarks</span></span>

<span data-ttu-id="70257-114">聲場回顯取消 (AEC) 演算法取決於音訊串流上的精確時間戳記。</span><span class="sxs-lookup"><span data-stu-id="70257-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="70257-115">事實上，時間戳記通常是完美的，而不同的音訊裝置可能會顯示不同的變異數和漂移率。</span><span class="sxs-lookup"><span data-stu-id="70257-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="70257-116">啟用 AEC 時，DSP 會收集時間戳記的相關統計資料，並使用此資訊來彌補是否有不准確。</span><span class="sxs-lookup"><span data-stu-id="70257-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="70257-117">如果這個屬性的值為 VARIANT \_ TRUE，則 DSP 會儲存在登錄中收集的統計資料。</span><span class="sxs-lookup"><span data-stu-id="70257-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="70257-118">下一次 DSP 使用同一組音訊裝置執行 AEC 時，會從登錄讀取統計資訊，讓 DSP 更有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="70257-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="70257-119">如果您將這個屬性的值設為 VARIANT \_ TRUE，並且在篩選模式中使用 DSP，您也應該設定 [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="70257-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="70257-120">在來源模式中，這不是必要的。</span><span class="sxs-lookup"><span data-stu-id="70257-120">In source mode, this is not required.</span></span>

<span data-ttu-id="70257-121">這個屬性的預設值為 VARIANT \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="70257-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="70257-122">只有在啟用 AEC 處理時，DSP 才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="70257-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="70257-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="70257-123">Requirements</span></span>



| <span data-ttu-id="70257-124">需求</span><span class="sxs-lookup"><span data-stu-id="70257-124">Requirement</span></span> | <span data-ttu-id="70257-125">值</span><span class="sxs-lookup"><span data-stu-id="70257-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70257-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70257-126">Minimum supported client</span></span><br/> | <span data-ttu-id="70257-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70257-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="70257-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70257-128">Minimum supported server</span></span><br/> | <span data-ttu-id="70257-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70257-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70257-130">標頭</span><span class="sxs-lookup"><span data-stu-id="70257-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="70257-131"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="70257-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70257-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70257-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70257-133">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="70257-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="70257-134">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="70257-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
