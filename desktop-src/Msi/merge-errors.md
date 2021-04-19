---
description: Merge 物件的唯讀錯誤屬性會傳回錯誤物件的集合，這些是一組目前的錯誤。
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: 'Merge。 Errors 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995290"
---
# <a name="mergeerrors-property"></a><span data-ttu-id="b19d7-103">Merge。 Errors 屬性</span><span class="sxs-lookup"><span data-stu-id="b19d7-103">Merge.Errors property</span></span>

<span data-ttu-id="b19d7-104">[**Merge**](merge-object.md)物件的唯讀 **錯誤** 屬性會傳回 [**錯誤**](error-object.md)物件的集合，這些是一組目前的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b19d7-104">The read-only **Errors** property of the [**Merge**](merge-object.md) object returns a collection of [**Error**](error-object.md) objects that is the current set of errors.</span></span>

<span data-ttu-id="b19d7-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b19d7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19d7-106">語法</span><span class="sxs-lookup"><span data-stu-id="b19d7-106">Syntax</span></span>


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a><span data-ttu-id="b19d7-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="b19d7-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b19d7-108">備註</span><span class="sxs-lookup"><span data-stu-id="b19d7-108">Remarks</span></span>

<span data-ttu-id="b19d7-109">抓取是非破壞性的。</span><span class="sxs-lookup"><span data-stu-id="b19d7-109">The retrieval is non-destructive.</span></span> <span data-ttu-id="b19d7-110">重複呼叫這個方法，即可抓取錯誤集合的多個實例。</span><span class="sxs-lookup"><span data-stu-id="b19d7-110">Multiple instances of the error collection may be retrieved by repeatedly calling this method.</span></span>

### <a name="c"></a><span data-ttu-id="b19d7-111">C++</span><span class="sxs-lookup"><span data-stu-id="b19d7-111">C++</span></span>

<span data-ttu-id="b19d7-112">請參閱 [**取得 \_ 錯誤**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) 函式。</span><span class="sxs-lookup"><span data-stu-id="b19d7-112">See [**get\_Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19d7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b19d7-113">Requirements</span></span>



| <span data-ttu-id="b19d7-114">需求</span><span class="sxs-lookup"><span data-stu-id="b19d7-114">Requirement</span></span> | <span data-ttu-id="b19d7-115">值</span><span class="sxs-lookup"><span data-stu-id="b19d7-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b19d7-116">版本</span><span class="sxs-lookup"><span data-stu-id="b19d7-116">Version</span></span><br/> | <span data-ttu-id="b19d7-117">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b19d7-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b19d7-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b19d7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b19d7-119"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="b19d7-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b19d7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b19d7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="b19d7-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b19d7-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
