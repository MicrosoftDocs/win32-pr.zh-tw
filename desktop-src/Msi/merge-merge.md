---
description: Merge 物件的 Merge 方法會執行目前資料庫和目前模組的合併。
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: 'Merge 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995463"
---
# <a name="mergemerge-method"></a><span data-ttu-id="4a202-103">Merge 方法</span><span class="sxs-lookup"><span data-stu-id="4a202-103">Merge.Merge method</span></span>

<span data-ttu-id="4a202-104">[**Merge**](merge-object.md)物件的 **merge** 方法會執行目前資料庫和目前模組的合併。</span><span class="sxs-lookup"><span data-stu-id="4a202-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="4a202-105">合併會將模組中的元件附加至 *功能* 所識別的功能。</span><span class="sxs-lookup"><span data-stu-id="4a202-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="4a202-106">模組目錄樹狀結構的根會重新導向至 *RedirectDir* 所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="4a202-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="4a202-107">**合併** 方法只能呼叫一次，以合併 .msi 和 .msm 檔案的特定組合。</span><span class="sxs-lookup"><span data-stu-id="4a202-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a202-108">語法</span><span class="sxs-lookup"><span data-stu-id="4a202-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="4a202-109">參數</span><span class="sxs-lookup"><span data-stu-id="4a202-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a202-110">*功能*</span><span class="sxs-lookup"><span data-stu-id="4a202-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="4a202-111">資料庫中的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="4a202-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="4a202-112">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="4a202-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="4a202-113">資料庫 [目錄資料表](directory-table.md) 中專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="4a202-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="4a202-114">這個參數可以是 null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="4a202-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a202-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a202-115">Return value</span></span>

<span data-ttu-id="4a202-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4a202-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a202-117">備註</span><span class="sxs-lookup"><span data-stu-id="4a202-117">Remarks</span></span>

<span data-ttu-id="4a202-118">完成合併之後，模組中的元件會附加至 *功能* 所識別的功能。</span><span class="sxs-lookup"><span data-stu-id="4a202-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="4a202-119">這項功能不會建立，且必須是現有的功能。</span><span class="sxs-lookup"><span data-stu-id="4a202-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="4a202-120">請注意， **Merge** 方法會取得模組中的所有功能參考，並針對模組資料庫中所有出現的 null GUID 取代功能參考。</span><span class="sxs-lookup"><span data-stu-id="4a202-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="4a202-121">如需詳細資訊，請參閱 [合併模組中的參考功能](referencing-features-in-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="4a202-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="4a202-122">您可以使用 [**Connect**](merge-connect.md) 方法將模組附加至其他功能。</span><span class="sxs-lookup"><span data-stu-id="4a202-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="4a202-123">請注意，呼叫 **Connect** 方法只會建立功能元件關聯。</span><span class="sxs-lookup"><span data-stu-id="4a202-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="4a202-124">它不會修改已合併至資料庫的資料列。</span><span class="sxs-lookup"><span data-stu-id="4a202-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="4a202-125">只有在呼叫 [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) 方法並將 *BCommit* 設為 **TRUE** 時，才會儲存對資料庫所做的變更。</span><span class="sxs-lookup"><span data-stu-id="4a202-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="4a202-126">如果發生任何合併衝突（包括排除），則會將它們放在錯誤列舉值中供稍後抓取，但不會導致合併失敗。</span><span class="sxs-lookup"><span data-stu-id="4a202-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="4a202-127">錯誤可能會透過 [ [**錯誤**](error-object.md) ] 屬性來抓取。</span><span class="sxs-lookup"><span data-stu-id="4a202-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="4a202-128">錯誤和參考用訊息會張貼至目前的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="4a202-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="4a202-129">C++</span><span class="sxs-lookup"><span data-stu-id="4a202-129">C++</span></span>

<span data-ttu-id="4a202-130">請參閱 [**合併**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) 函數。</span><span class="sxs-lookup"><span data-stu-id="4a202-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a202-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a202-131">Requirements</span></span>



| <span data-ttu-id="4a202-132">需求</span><span class="sxs-lookup"><span data-stu-id="4a202-132">Requirement</span></span> | <span data-ttu-id="4a202-133">值</span><span class="sxs-lookup"><span data-stu-id="4a202-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a202-134">版本</span><span class="sxs-lookup"><span data-stu-id="4a202-134">Version</span></span><br/> | <span data-ttu-id="4a202-135">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4a202-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="4a202-136">標頭</span><span class="sxs-lookup"><span data-stu-id="4a202-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4a202-137"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a202-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a202-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4a202-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a202-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a202-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
