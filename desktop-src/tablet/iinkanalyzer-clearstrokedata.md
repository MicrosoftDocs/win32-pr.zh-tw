---
description: 清除 IInkAnalyzer 中的筆觸封包資料。
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'IInkAnalyzer：： ClearStrokeData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469128"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="19dc9-103">IInkAnalyzer：： ClearStrokeData 方法</span><span class="sxs-lookup"><span data-stu-id="19dc9-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="19dc9-104">清除 [**IInkAnalyzer**](iinkanalyzer.md)中的筆觸封包資料。</span><span class="sxs-lookup"><span data-stu-id="19dc9-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19dc9-105">語法</span><span class="sxs-lookup"><span data-stu-id="19dc9-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="19dc9-106">參數</span><span class="sxs-lookup"><span data-stu-id="19dc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19dc9-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19dc9-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19dc9-108">已清除封包資料之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="19dc9-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19dc9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="19dc9-109">Return value</span></span>

<span data-ttu-id="19dc9-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="19dc9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19dc9-111">備註</span><span class="sxs-lookup"><span data-stu-id="19dc9-111">Remarks</span></span>

<span data-ttu-id="19dc9-112">當筆觸的封包資料變更時（例如移動或轉換筆劃時），請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="19dc9-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="19dc9-113">當 [**IInkAnalyzer**](iinkanalyzer.md)需要筆劃封包資料來自已清除封包資料的筆劃時，就會引發 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件。</span><span class="sxs-lookup"><span data-stu-id="19dc9-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="19dc9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="19dc9-114">Requirements</span></span>



| <span data-ttu-id="19dc9-115">需求</span><span class="sxs-lookup"><span data-stu-id="19dc9-115">Requirement</span></span> | <span data-ttu-id="19dc9-116">值</span><span class="sxs-lookup"><span data-stu-id="19dc9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19dc9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19dc9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19dc9-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19dc9-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="19dc9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19dc9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19dc9-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="19dc9-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="19dc9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="19dc9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="19dc9-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="19dc9-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="19dc9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="19dc9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19dc9-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19dc9-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="19dc9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19dc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19dc9-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="19dc9-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="19dc9-127">**IInkAnalyzer：： UpdateStrokesData 方法**</span><span class="sxs-lookup"><span data-stu-id="19dc9-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="19dc9-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="19dc9-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




