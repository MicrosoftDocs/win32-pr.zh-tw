---
description: 更新指定筆劃的封包資料。
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'IInkAnalyzer：： UpdateStrokesData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972429"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="f8014-103">IInkAnalyzer：： UpdateStrokesData 方法</span><span class="sxs-lookup"><span data-stu-id="f8014-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="f8014-104">更新指定筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="f8014-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8014-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8014-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="f8014-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8014-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8014-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8014-108">要更新的筆觸數目。</span><span class="sxs-lookup"><span data-stu-id="f8014-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="f8014-109">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8014-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8014-110">包含筆觸識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="f8014-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f8014-111">*ulStrokePacketDescriptionCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8014-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8014-112">每個封包中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="f8014-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="f8014-113">*pStrokePacketDescriptionGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8014-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8014-114">陣列，包含封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8014-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="f8014-115">*pulPacketDataCountPerStroke* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8014-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8014-116">陣列，其中包含每個筆劃中的封包數目。</span><span class="sxs-lookup"><span data-stu-id="f8014-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="f8014-117">*plStrokePacketData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8014-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8014-118">陣列，其中包含筆觸的封包資料。</span><span class="sxs-lookup"><span data-stu-id="f8014-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8014-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8014-119">Return value</span></span>

<span data-ttu-id="f8014-120">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f8014-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8014-121">備註</span><span class="sxs-lookup"><span data-stu-id="f8014-121">Remarks</span></span>

<span data-ttu-id="f8014-122">*plStrokePacketData* 參數包含所有筆劃的封包資料。</span><span class="sxs-lookup"><span data-stu-id="f8014-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="f8014-123">*PStrokePacketDescriptionGuids* 參數包含 (guid) 的全域唯一識別碼，描述每個筆劃中每個點所包含的封包資料類型。</span><span class="sxs-lookup"><span data-stu-id="f8014-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="f8014-124">如需可用的封包屬性完整清單，請參閱 [PacketPropertyGuids 常數](packetpropertyguids-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="f8014-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="f8014-125">只有具有相同封包描述的筆觸可以在 **IInkAnalyzer：： UpdateStrokesData 方法** 的單一呼叫中更新。</span><span class="sxs-lookup"><span data-stu-id="f8014-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="f8014-126">這個方法不會更新筆墨分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f8014-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="f8014-127">如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會忽略識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8014-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="f8014-128">如果任何指定的筆觸都沒有識別與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆劃，這個方法會傳回而不更新 **IInkAnalyzer**。</span><span class="sxs-lookup"><span data-stu-id="f8014-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="f8014-129">當 *plStrokeIds* 為 **Null** 時，這個方法會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f8014-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8014-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8014-130">Requirements</span></span>



| <span data-ttu-id="f8014-131">需求</span><span class="sxs-lookup"><span data-stu-id="f8014-131">Requirement</span></span> | <span data-ttu-id="f8014-132">值</span><span class="sxs-lookup"><span data-stu-id="f8014-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8014-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8014-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8014-134">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8014-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f8014-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8014-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8014-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="f8014-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f8014-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f8014-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8014-138"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f8014-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f8014-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f8014-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8014-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8014-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f8014-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8014-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8014-142">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f8014-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f8014-143">**IInkAnalyzer：： AddStroke 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="f8014-144">**IInkAnalyzer：： AddStrokeForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f8014-145">**IInkAnalyzer：： AddStrokeToCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="f8014-146">**IInkAnalyzer：： AddStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="f8014-147">**IInkAnalyzer：： AddStrokesForLanguage 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f8014-148">**IInkAnalyzer：： AddStrokesToCustomRecognizer 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="f8014-149">**IInkAnalyzer：： ClearStrokeData 方法**</span><span class="sxs-lookup"><span data-stu-id="f8014-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="f8014-150">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="f8014-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="f8014-151">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="f8014-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




