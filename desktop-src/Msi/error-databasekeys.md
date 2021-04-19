---
description: Error 物件的唯讀 DatabaseKeys 屬性會傳回字串集合，其中包含造成錯誤之資料庫資料列的主鍵。 集合中的每個專案都有一個金鑰。
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: '錯誤。 DatabaseKeys 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989247"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="d9b4a-104">錯誤。 DatabaseKeys 屬性</span><span class="sxs-lookup"><span data-stu-id="d9b4a-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="d9b4a-105">[**Error**](error-object.md)物件的唯讀 **DatabaseKeys** 屬性會傳回字串集合，其中包含造成錯誤之資料庫資料列的主鍵。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="d9b4a-106">集合中的每個專案都有一個金鑰。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="d9b4a-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b4a-108">語法</span><span class="sxs-lookup"><span data-stu-id="d9b4a-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="d9b4a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d9b4a-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b4a-110">備註</span><span class="sxs-lookup"><span data-stu-id="d9b4a-110">Remarks</span></span>

<span data-ttu-id="d9b4a-111">當不再需要時，用戶端會負責釋放字串集合。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="d9b4a-112">如果值不適用於錯誤的類型，則集合是空的。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="d9b4a-113">您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="d9b4a-114">C++</span><span class="sxs-lookup"><span data-stu-id="d9b4a-114">C++</span></span>

<span data-ttu-id="d9b4a-115">請參閱 [**get \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) 函式。</span><span class="sxs-lookup"><span data-stu-id="d9b4a-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b4a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9b4a-116">Requirements</span></span>



| <span data-ttu-id="d9b4a-117">需求</span><span class="sxs-lookup"><span data-stu-id="d9b4a-117">Requirement</span></span> | <span data-ttu-id="d9b4a-118">值</span><span class="sxs-lookup"><span data-stu-id="d9b4a-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b4a-119">版本</span><span class="sxs-lookup"><span data-stu-id="d9b4a-119">Version</span></span><br/> | <span data-ttu-id="d9b4a-120">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d9b4a-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d9b4a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d9b4a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d9b4a-122"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b4a-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9b4a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d9b4a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9b4a-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9b4a-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 

