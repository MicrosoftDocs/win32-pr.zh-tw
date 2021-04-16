---
description: 抓取檔的區域，該區域對應于 IInkAnalyzer 物件的內容節點樹狀結構中，做為筆跡分析結果的變更。
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'IAnalysisStatus：： GetAppliedChangesRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511692"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="8cf2d-103">IAnalysisStatus：： GetAppliedChangesRegion 方法</span><span class="sxs-lookup"><span data-stu-id="8cf2d-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="8cf2d-104">抓取檔的區域，該區域對應于 [**IInkAnalyzer**](iinkanalyzer.md) 物件的內容節點樹狀結構中，做為筆跡分析結果的變更。</span><span class="sxs-lookup"><span data-stu-id="8cf2d-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8cf2d-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="8cf2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8cf2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf2d-107">*pAppliedChangesRegion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8cf2d-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf2d-108">已進行變更之檔的 [**IAnalysisRegion**](ianalysisregion.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="8cf2d-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf2d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cf2d-109">Return value</span></span>

<span data-ttu-id="8cf2d-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8cf2d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf2d-111">備註</span><span class="sxs-lookup"><span data-stu-id="8cf2d-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8cf2d-112">若要避免記憶體流失，請在 pAppliedChangesRegion 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要流量分析區域時）。</span><span class="sxs-lookup"><span data-stu-id="8cf2d-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="8cf2d-113">當應用程式收到用於偵測的資訊，而且需要使變更可能發生，以便繪製偵錯工具資訊時，最常使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="8cf2d-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf2d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cf2d-114">Requirements</span></span>



| <span data-ttu-id="8cf2d-115">需求</span><span class="sxs-lookup"><span data-stu-id="8cf2d-115">Requirement</span></span> | <span data-ttu-id="8cf2d-116">值</span><span class="sxs-lookup"><span data-stu-id="8cf2d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf2d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8cf2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf2d-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cf2d-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cf2d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8cf2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf2d-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="8cf2d-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8cf2d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8cf2d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf2d-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8cf2d-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cf2d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8cf2d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cf2d-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cf2d-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8cf2d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cf2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf2d-126">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="8cf2d-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="8cf2d-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="8cf2d-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="8cf2d-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8cf2d-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

