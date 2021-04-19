---
description: 相依性物件的唯讀模組屬性會傳回目前字串（以 BSTR 形式）所需的模組 ModuleID。 ModuleID 是在 ModuleSignature 資料表中使用的相同形式。
ms.assetid: 22aae1b6-59b6-4842-9523-d1e064511380
title: '相依性。 Module 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency.Module
- IMsmDependency.get_Module
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4bcf2241cd278640b333bb9f08dc24e645990b4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991184"
---
# <a name="dependencymodule-property"></a><span data-ttu-id="e9708-104">相依性。 Module 屬性</span><span class="sxs-lookup"><span data-stu-id="e9708-104">Dependency.Module property</span></span>

<span data-ttu-id="e9708-105">相依性 [**物件**](dependency-object.md)的唯讀 **模組** 屬性會傳回目前字串（以 **BSTR** 形式）所需的模組 ModuleID。</span><span class="sxs-lookup"><span data-stu-id="e9708-105">The read-only **Module** property of the [**Dependency Object**](dependency-object.md) returns the ModuleID of the module that is required by the current string in the form of a **BSTR**.</span></span> <span data-ttu-id="e9708-106">ModuleID 是在 [ModuleSignature 資料表](modulesignature-table.md)中使用的相同形式。</span><span class="sxs-lookup"><span data-stu-id="e9708-106">The ModuleID is the same form that is used in the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="e9708-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e9708-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9708-108">語法</span><span class="sxs-lookup"><span data-stu-id="e9708-108">Syntax</span></span>


```JScript
propVal = Dependency.Module
```



## <a name="property-value"></a><span data-ttu-id="e9708-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e9708-109">Property value</span></span>

## <a name="c"></a><span data-ttu-id="e9708-110">C++</span><span class="sxs-lookup"><span data-stu-id="e9708-110">C++</span></span>

<span data-ttu-id="e9708-111">請參閱 [**IMsmDependency \_ 取得 \_ 模組**](/windows/win32/api/mergemod/nf-mergemod-imsmdependency-get_module) 方法。</span><span class="sxs-lookup"><span data-stu-id="e9708-111">See the [**IMsmDependency\_get\_Module**](/windows/win32/api/mergemod/nf-mergemod-imsmdependency-get_module) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9708-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9708-112">Requirements</span></span>



| <span data-ttu-id="e9708-113">需求</span><span class="sxs-lookup"><span data-stu-id="e9708-113">Requirement</span></span> | <span data-ttu-id="e9708-114">值</span><span class="sxs-lookup"><span data-stu-id="e9708-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9708-115">版本</span><span class="sxs-lookup"><span data-stu-id="e9708-115">Version</span></span><br/> | <span data-ttu-id="e9708-116">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e9708-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e9708-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e9708-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9708-118"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9708-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9708-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e9708-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9708-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9708-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

