---
description: Merge 物件的 [唯讀相依性] 屬性會傳回相依性物件的集合，這些物件會列舉目前資料庫的一組未滿足的相依性。
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: 'Merge。相依性屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977702"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="cc2b1-103">Merge。相依性屬性</span><span class="sxs-lookup"><span data-stu-id="cc2b1-103">Merge.Dependencies property</span></span>

<span data-ttu-id="cc2b1-104">[**Merge**](merge-object.md)物件的 [唯讀相依性 **]** 屬性會傳回相依性物件 [**的集合，這些物件會**](dependency-object.md)列舉目前資料庫的一組未滿足的相依性。</span><span class="sxs-lookup"><span data-stu-id="cc2b1-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="cc2b1-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cc2b1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc2b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="cc2b1-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="cc2b1-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="cc2b1-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="cc2b1-108">備註</span><span class="sxs-lookup"><span data-stu-id="cc2b1-108">Remarks</span></span>

<span data-ttu-id="cc2b1-109">不需要開啟模組就能取出相依性資訊。</span><span class="sxs-lookup"><span data-stu-id="cc2b1-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="cc2b1-110">C++</span><span class="sxs-lookup"><span data-stu-id="cc2b1-110">C++</span></span>

<span data-ttu-id="cc2b1-111">請 [**參閱 \_ 取得**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) 相依性功能。</span><span class="sxs-lookup"><span data-stu-id="cc2b1-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc2b1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc2b1-112">Requirements</span></span>



| <span data-ttu-id="cc2b1-113">需求</span><span class="sxs-lookup"><span data-stu-id="cc2b1-113">Requirement</span></span> | <span data-ttu-id="cc2b1-114">值</span><span class="sxs-lookup"><span data-stu-id="cc2b1-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc2b1-115">版本</span><span class="sxs-lookup"><span data-stu-id="cc2b1-115">Version</span></span><br/> | <span data-ttu-id="cc2b1-116">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cc2b1-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="cc2b1-117">標頭</span><span class="sxs-lookup"><span data-stu-id="cc2b1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cc2b1-118"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc2b1-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc2b1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="cc2b1-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc2b1-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc2b1-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
