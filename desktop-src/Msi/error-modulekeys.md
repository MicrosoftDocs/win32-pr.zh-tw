---
description: Error 物件的唯讀 ModuleKeys 屬性會傳回字串集合的指標，其中包含模組中資料列的主鍵，而該資料列會造成錯誤，也就是集合中每個專案的一個索引鍵。
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: '錯誤。 ModuleKeys 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999164"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="04b3b-103">錯誤。 ModuleKeys 屬性</span><span class="sxs-lookup"><span data-stu-id="04b3b-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="04b3b-104">[**Error**](error-object.md)物件的唯讀 **ModuleKeys** 屬性會傳回字串集合的指標，其中包含模組中資料列的主鍵，而該資料列會造成錯誤，也就是集合中每個專案的一個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="04b3b-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="04b3b-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="04b3b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b3b-106">語法</span><span class="sxs-lookup"><span data-stu-id="04b3b-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="04b3b-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="04b3b-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="04b3b-108">備註</span><span class="sxs-lookup"><span data-stu-id="04b3b-108">Remarks</span></span>

<span data-ttu-id="04b3b-109">當不再需要時，用戶端會負責釋放字串集合。</span><span class="sxs-lookup"><span data-stu-id="04b3b-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="04b3b-110">如果值不適用於錯誤的類型，則集合是空的。</span><span class="sxs-lookup"><span data-stu-id="04b3b-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="04b3b-111">您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="04b3b-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="04b3b-112">C++</span><span class="sxs-lookup"><span data-stu-id="04b3b-112">C++</span></span>

<span data-ttu-id="04b3b-113">請參閱 [**get \_ ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) 函式。</span><span class="sxs-lookup"><span data-stu-id="04b3b-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b3b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="04b3b-114">Requirements</span></span>



| <span data-ttu-id="04b3b-115">需求</span><span class="sxs-lookup"><span data-stu-id="04b3b-115">Requirement</span></span> | <span data-ttu-id="04b3b-116">值</span><span class="sxs-lookup"><span data-stu-id="04b3b-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b3b-117">版本</span><span class="sxs-lookup"><span data-stu-id="04b3b-117">Version</span></span><br/> | <span data-ttu-id="04b3b-118">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="04b3b-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="04b3b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="04b3b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="04b3b-120"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="04b3b-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="04b3b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="04b3b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="04b3b-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b3b-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

