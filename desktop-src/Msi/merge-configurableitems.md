---
description: Merge 物件的唯讀 ConfigurableItems 屬性會傳回集合 ConfigurableItem 物件，每個物件都代表 ModuleConfiguration 資料表中的單一資料列。
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: 'Merge.ConfigurableItems 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999338"
---
# <a name="mergeconfigurableitems-property"></a><span data-ttu-id="19e64-103">Merge.ConfigurableItems 屬性</span><span class="sxs-lookup"><span data-stu-id="19e64-103">Merge.ConfigurableItems property</span></span>

<span data-ttu-id="19e64-104">[**Merge**](merge-object.md)物件的唯讀 **ConfigurableItems** 屬性會傳回集合 [**ConfigurableItem**](configurableitem-object.md)物件，每個物件都代表 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的單一資料列。</span><span class="sxs-lookup"><span data-stu-id="19e64-104">The read-only **ConfigurableItems** property of the [**Merge**](merge-object.md) object returns a collection [**ConfigurableItem**](configurableitem-object.md) objects, each of which represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="19e64-105">就語義而言，列舉值中的每個介面都代表一個可由模組取用者設定的專案。</span><span class="sxs-lookup"><span data-stu-id="19e64-105">Semantically, each interface in the enumerator represents an item that can be configured by the module consumer.</span></span> <span data-ttu-id="19e64-106">集合是唯讀的集合，並會執行專案 () 、計數 () 和 NewEnum () 的標準唯讀集合介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="19e64-106">The collection is a read-only collection and implements the standard read-only collection interfaces of Item(), Count() and \_NewEnum().</span></span> <span data-ttu-id="19e64-107">**IEnumMsmConfigItems** 列舉值會使用標準語義來執行下一個 () 、略過 () 、重設 () 和複製 () 。</span><span class="sxs-lookup"><span data-stu-id="19e64-107">The **IEnumMsmConfigItems** enumerator implements Next(), Skip(), Reset(), and Clone() with the standard semantics.</span></span>

<span data-ttu-id="19e64-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="19e64-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e64-109">語法</span><span class="sxs-lookup"><span data-stu-id="19e64-109">Syntax</span></span>


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a><span data-ttu-id="19e64-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="19e64-110">Property value</span></span>

## <a name="c"></a><span data-ttu-id="19e64-111">C++</span><span class="sxs-lookup"><span data-stu-id="19e64-111">C++</span></span>

<span data-ttu-id="19e64-112">請參閱 [**get \_ ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) 函式。</span><span class="sxs-lookup"><span data-stu-id="19e64-112">See [**get\_ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e64-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e64-113">Requirements</span></span>



| <span data-ttu-id="19e64-114">需求</span><span class="sxs-lookup"><span data-stu-id="19e64-114">Requirement</span></span> | <span data-ttu-id="19e64-115">值</span><span class="sxs-lookup"><span data-stu-id="19e64-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19e64-116">版本</span><span class="sxs-lookup"><span data-stu-id="19e64-116">Version</span></span><br/> | <span data-ttu-id="19e64-117">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="19e64-117">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="19e64-118">標頭</span><span class="sxs-lookup"><span data-stu-id="19e64-118">Header</span></span><br/>  | <dl> <span data-ttu-id="19e64-119"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="19e64-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="19e64-120">DLL</span><span class="sxs-lookup"><span data-stu-id="19e64-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="19e64-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e64-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




