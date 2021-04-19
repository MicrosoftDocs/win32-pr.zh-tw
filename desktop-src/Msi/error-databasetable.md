---
description: Error 物件的唯讀 DatabaseTable 屬性會傳回資料庫中造成錯誤之資料表的名稱。
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: '錯誤。 DatabaseTable 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989246"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="f5573-103">錯誤。 DatabaseTable 屬性</span><span class="sxs-lookup"><span data-stu-id="f5573-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="f5573-104">[**Error**](error-object.md)物件的唯讀 **DatabaseTable** 屬性會傳回資料庫中造成錯誤之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5573-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="f5573-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f5573-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5573-106">語法</span><span class="sxs-lookup"><span data-stu-id="f5573-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="f5573-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f5573-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f5573-108">備註</span><span class="sxs-lookup"><span data-stu-id="f5573-108">Remarks</span></span>

<span data-ttu-id="f5573-109">如果值不適用於錯誤的類型，則集合是空的。</span><span class="sxs-lookup"><span data-stu-id="f5573-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="f5573-110">您可以藉由呼叫 [**error**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="f5573-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="f5573-111">C++</span><span class="sxs-lookup"><span data-stu-id="f5573-111">C++</span></span>

<span data-ttu-id="f5573-112">請參閱 [**get \_ DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) 函式。</span><span class="sxs-lookup"><span data-stu-id="f5573-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5573-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5573-113">Requirements</span></span>



| <span data-ttu-id="f5573-114">需求</span><span class="sxs-lookup"><span data-stu-id="f5573-114">Requirement</span></span> | <span data-ttu-id="f5573-115">值</span><span class="sxs-lookup"><span data-stu-id="f5573-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5573-116">版本</span><span class="sxs-lookup"><span data-stu-id="f5573-116">Version</span></span><br/> | <span data-ttu-id="f5573-117">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f5573-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="f5573-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f5573-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f5573-119"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5573-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5573-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f5573-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5573-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5573-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

