---
description: 抓取指定之筆劃的型別。
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'IInkAnalyzer：： GetStrokeType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191403"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="8ca08-103">IInkAnalyzer：： GetStrokeType 方法</span><span class="sxs-lookup"><span data-stu-id="8ca08-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="8ca08-104">抓取指定之筆劃的型別。</span><span class="sxs-lookup"><span data-stu-id="8ca08-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca08-105">語法</span><span class="sxs-lookup"><span data-stu-id="8ca08-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="8ca08-106">參數</span><span class="sxs-lookup"><span data-stu-id="8ca08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca08-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ca08-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca08-108">筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ca08-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8ca08-109">*pStrokeType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8ca08-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca08-110">指定之筆劃的分類。</span><span class="sxs-lookup"><span data-stu-id="8ca08-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca08-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ca08-111">Return value</span></span>

<span data-ttu-id="8ca08-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca08-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca08-113">備註</span><span class="sxs-lookup"><span data-stu-id="8ca08-113">Remarks</span></span>

<span data-ttu-id="8ca08-114">如果筆劃的類型是 [**StrokeType**](stroketype.md) 值 StrokeType 非 \_ 分類，則 [**IInkAnalyzer**](iinkanalyzer.md) 會在筆跡分析期間將筆劃分類。</span><span class="sxs-lookup"><span data-stu-id="8ca08-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="8ca08-115">否則， **IInkAnalyzer** 會使用筆劃上設定的類型。</span><span class="sxs-lookup"><span data-stu-id="8ca08-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="8ca08-116">[**IInkAnalyzer**](iinkanalyzer.md)不會將筆劃類型值設定為筆跡分析的一部分。</span><span class="sxs-lookup"><span data-stu-id="8ca08-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="8ca08-117">若要指定或變更筆觸類型，請使用 [**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md) 或 [**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca08-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca08-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca08-118">Requirements</span></span>



| <span data-ttu-id="8ca08-119">需求</span><span class="sxs-lookup"><span data-stu-id="8ca08-119">Requirement</span></span> | <span data-ttu-id="8ca08-120">值</span><span class="sxs-lookup"><span data-stu-id="8ca08-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca08-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ca08-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca08-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca08-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ca08-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ca08-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca08-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="8ca08-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8ca08-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8ca08-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca08-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8ca08-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ca08-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca08-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ca08-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca08-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8ca08-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ca08-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca08-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8ca08-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8ca08-131">**IInkAnalyzer：： SetStrokeType 方法**</span><span class="sxs-lookup"><span data-stu-id="8ca08-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="8ca08-132">**IInkAnalyzer：： SetStrokesType 方法**</span><span class="sxs-lookup"><span data-stu-id="8ca08-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="8ca08-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8ca08-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




