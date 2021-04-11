---
description: 抓取位元組陣列，其中包含此 ICoNtextNode 的應用程式特定和內部屬性資料。
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'ICoNtextNode：： SavePropertiesData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943470"
---
# <a name="icontextnodesavepropertiesdata-method"></a><span data-ttu-id="a9075-103">ICoNtextNode：： SavePropertiesData 方法</span><span class="sxs-lookup"><span data-stu-id="a9075-103">IContextNode::SavePropertiesData method</span></span>

<span data-ttu-id="a9075-104">抓取位元組陣列，其中包含此 [**ICoNtextNode**](icontextnode.md)的應用程式特定和內部屬性資料。</span><span class="sxs-lookup"><span data-stu-id="a9075-104">Retrieves an array of bytes that contains the application-specific and internal property data for this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9075-105">語法</span><span class="sxs-lookup"><span data-stu-id="a9075-105">Syntax</span></span>


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="a9075-106">參數</span><span class="sxs-lookup"><span data-stu-id="a9075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9075-107">*pulPropertiesDataSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a9075-107">*pulPropertiesDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9075-108">包含屬性資訊之資料陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="a9075-108">The size of the data array containing the property information.</span></span> <span data-ttu-id="a9075-109">未使用傳入的值。</span><span class="sxs-lookup"><span data-stu-id="a9075-109">The value passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a9075-110">*ppbPropertiesData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9075-110">*ppbPropertiesData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9075-111">8位不帶正負號的整數陣列的指標，其中包含應用程式特定和內部屬性資料。</span><span class="sxs-lookup"><span data-stu-id="a9075-111">A pointer to an 8-bit unsigned integer array that contains the application-specific and internal property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9075-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9075-112">Return value</span></span>

<span data-ttu-id="a9075-113">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="a9075-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a9075-114">備註</span><span class="sxs-lookup"><span data-stu-id="a9075-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a9075-115">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppbPropertiesData* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a9075-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertiesData* when you no longer need the information.</span></span>

 

<span data-ttu-id="a9075-116">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="a9075-116">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="a9075-117">這個方法會儲存 **IInkAnalyzer** 在 [**ICoNtextNode**](icontextnode.md)上設定的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="a9075-117">This method saves the property data that the **IInkAnalyzer** has set on the [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="a9075-118">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="a9075-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9075-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9075-119">Requirements</span></span>



| <span data-ttu-id="a9075-120">需求</span><span class="sxs-lookup"><span data-stu-id="a9075-120">Requirement</span></span> | <span data-ttu-id="a9075-121">值</span><span class="sxs-lookup"><span data-stu-id="a9075-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9075-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9075-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9075-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9075-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a9075-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9075-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9075-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="a9075-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a9075-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a9075-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9075-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a9075-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a9075-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a9075-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9075-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9075-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a9075-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9075-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9075-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="a9075-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a9075-132">**ICoNtextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="a9075-132">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="a9075-133">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a9075-133">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a9075-134">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a9075-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="a9075-135">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="a9075-135">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="a9075-136">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="a9075-136">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="a9075-137">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="a9075-137">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="a9075-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="a9075-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

