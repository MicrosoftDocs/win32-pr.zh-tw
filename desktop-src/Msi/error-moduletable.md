---
description: 唯讀 ModuleTable 屬性會傳回模組中造成錯誤之資料表的名稱。
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: '錯誤。 ModuleTable 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978648"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="13d4e-103">錯誤。 ModuleTable 屬性</span><span class="sxs-lookup"><span data-stu-id="13d4e-103">Error.ModuleTable property</span></span>

<span data-ttu-id="13d4e-104">唯讀 **ModuleTable** 屬性會傳回模組中造成錯誤之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="13d4e-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="13d4e-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="13d4e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d4e-106">語法</span><span class="sxs-lookup"><span data-stu-id="13d4e-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="13d4e-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="13d4e-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="13d4e-108">備註</span><span class="sxs-lookup"><span data-stu-id="13d4e-108">Remarks</span></span>

<span data-ttu-id="13d4e-109">如果值不適用於錯誤的類型，則集合是空的。</span><span class="sxs-lookup"><span data-stu-id="13d4e-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="13d4e-110">您可以藉由呼叫 [**錯誤**](error-object.md)物件的 [**type**](error-type.md)屬性來判斷錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="13d4e-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="13d4e-111">C++</span><span class="sxs-lookup"><span data-stu-id="13d4e-111">C++</span></span>

<span data-ttu-id="13d4e-112">請參閱 [**get \_ ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) 函式。</span><span class="sxs-lookup"><span data-stu-id="13d4e-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d4e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="13d4e-113">Requirements</span></span>



| <span data-ttu-id="13d4e-114">需求</span><span class="sxs-lookup"><span data-stu-id="13d4e-114">Requirement</span></span> | <span data-ttu-id="13d4e-115">值</span><span class="sxs-lookup"><span data-stu-id="13d4e-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d4e-116">版本</span><span class="sxs-lookup"><span data-stu-id="13d4e-116">Version</span></span><br/> | <span data-ttu-id="13d4e-117">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="13d4e-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="13d4e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="13d4e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="13d4e-119"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="13d4e-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="13d4e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="13d4e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="13d4e-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13d4e-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

