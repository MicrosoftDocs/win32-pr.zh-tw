---
description: GetFiles 物件的 ModuleFiles 屬性會針對目前開啟的模組，傳回檔案資料表的所有主要索引鍵。
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: 'GetFiles. ModuleFiles 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997795"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="78134-103">GetFiles. ModuleFiles 屬性</span><span class="sxs-lookup"><span data-stu-id="78134-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="78134-104">[**GetFiles**](getfiles-object.md)物件的 **ModuleFiles** 屬性會針對目前開啟的模組，傳回檔案 [資料表](file-table.md)的所有主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="78134-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="78134-105">主要索引鍵會以字串集合的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="78134-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="78134-106">在呼叫 **ModuleFiles** 之前，必須先呼叫 [Merge 物件](merge-object.md)的 [**OpenModule**](merge-openmodule.md)方法來開啟模組。</span><span class="sxs-lookup"><span data-stu-id="78134-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="78134-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="78134-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78134-108">語法</span><span class="sxs-lookup"><span data-stu-id="78134-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="78134-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="78134-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="78134-110">備註</span><span class="sxs-lookup"><span data-stu-id="78134-110">Remarks</span></span>

<span data-ttu-id="78134-111">請注意，集合中列出的檔案順序可能不會與 File 資料表中所列的順序相同。</span><span class="sxs-lookup"><span data-stu-id="78134-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="78134-112">如果模組沒有檔案資料表，或不包含特定語言的任何檔案，ModuleFiles 會傳回空的字串集合。</span><span class="sxs-lookup"><span data-stu-id="78134-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="78134-113">C++</span><span class="sxs-lookup"><span data-stu-id="78134-113">C++</span></span>

<span data-ttu-id="78134-114">請參閱 [**get \_ ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) 函式。</span><span class="sxs-lookup"><span data-stu-id="78134-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="78134-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="78134-115">Requirements</span></span>



| <span data-ttu-id="78134-116">需求</span><span class="sxs-lookup"><span data-stu-id="78134-116">Requirement</span></span> | <span data-ttu-id="78134-117">值</span><span class="sxs-lookup"><span data-stu-id="78134-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78134-118">版本</span><span class="sxs-lookup"><span data-stu-id="78134-118">Version</span></span><br/> | <span data-ttu-id="78134-119">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="78134-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="78134-120">標頭</span><span class="sxs-lookup"><span data-stu-id="78134-120">Header</span></span><br/>  | <dl> <span data-ttu-id="78134-121"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="78134-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="78134-122">DLL</span><span class="sxs-lookup"><span data-stu-id="78134-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="78134-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78134-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
