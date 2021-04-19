---
description: Merge 物件的 MergeEx 方法相當於 Merge 函式，但它會接受額外的引數。
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: 'MergeEx 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995243"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="fd8af-103">Merge. MergeEx 方法</span><span class="sxs-lookup"><span data-stu-id="fd8af-103">Merge.MergeEx method</span></span>

<span data-ttu-id="fd8af-104">[**Merge**](merge-object.md)物件的 **MergeEx** 方法相當於 [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge)函式，但它會接受額外的引數。</span><span class="sxs-lookup"><span data-stu-id="fd8af-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="fd8af-105">*PConfiguration* 引數是用戶端所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="fd8af-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="fd8af-106">引數可以是 null。</span><span class="sxs-lookup"><span data-stu-id="fd8af-106">The argument may be null.</span></span> <span data-ttu-id="fd8af-107">此引數的存在表示用戶端能夠支援設定功能，但不會商都必須用戶端來提供任何特定可設定專案的設定資料。</span><span class="sxs-lookup"><span data-stu-id="fd8af-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="fd8af-108">[**Merge**](merge-merge.md)方法會執行目前資料庫和目前模組的合併。</span><span class="sxs-lookup"><span data-stu-id="fd8af-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="fd8af-109">合併會將模組中的元件附加至 *功能* 所識別的功能。</span><span class="sxs-lookup"><span data-stu-id="fd8af-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="fd8af-110">模組目錄樹狀結構的根會重新導向至 *RedirectDir* 所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="fd8af-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8af-111">語法</span><span class="sxs-lookup"><span data-stu-id="fd8af-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="fd8af-112">參數</span><span class="sxs-lookup"><span data-stu-id="fd8af-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8af-113">*功能*</span><span class="sxs-lookup"><span data-stu-id="fd8af-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="fd8af-114">資料庫中的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8af-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="fd8af-115">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="fd8af-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="fd8af-116">資料庫 [目錄資料表](directory-table.md) 中專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fd8af-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="fd8af-117">這個參數可以是 null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="fd8af-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="fd8af-118">*pConfiguration*</span><span class="sxs-lookup"><span data-stu-id="fd8af-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="fd8af-119">*PConfiguration* 引數是用戶端所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="fd8af-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="fd8af-120">引數可以是 null。</span><span class="sxs-lookup"><span data-stu-id="fd8af-120">The argument may be null.</span></span> <span data-ttu-id="fd8af-121">此引數的存在表示用戶端能夠支援設定功能，但不會商都必須用戶端來提供任何特定可設定專案的設定資料。</span><span class="sxs-lookup"><span data-stu-id="fd8af-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8af-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd8af-122">Return value</span></span>

<span data-ttu-id="fd8af-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fd8af-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8af-124">備註</span><span class="sxs-lookup"><span data-stu-id="fd8af-124">Remarks</span></span>

<span data-ttu-id="fd8af-125">完成合併之後，模組中的元件會附加至 *功能* 所識別的功能。</span><span class="sxs-lookup"><span data-stu-id="fd8af-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="fd8af-126">這項功能不會建立，且必須是現有的功能。</span><span class="sxs-lookup"><span data-stu-id="fd8af-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="fd8af-127">您可以使用 [**Connect**](merge-connect.md) 方法將模組附加至其他功能。</span><span class="sxs-lookup"><span data-stu-id="fd8af-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="fd8af-128">只有在呼叫 [**CloseDatabase**](merge-closedatabase.md) 方法並將 *BCommit* 設為 **TRUE** 時，才會儲存對資料庫所做的變更。</span><span class="sxs-lookup"><span data-stu-id="fd8af-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="fd8af-129">如果發生任何合併衝突（包括排除），則會將它們放在錯誤列舉值中供稍後抓取，但不會導致合併失敗。</span><span class="sxs-lookup"><span data-stu-id="fd8af-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="fd8af-130">錯誤可能會透過 [ [**錯誤**](merge-errors.md) ] 屬性來抓取。</span><span class="sxs-lookup"><span data-stu-id="fd8af-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="fd8af-131">錯誤和參考用訊息會張貼至目前的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="fd8af-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="fd8af-132">當合併因為模組設定不正確而失敗時， [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) 函數會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="fd8af-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="fd8af-133">這包括下列 msmErrorType 錯誤： **msmErrorBadNullSubstitution**、 **msmErrorBadSubstitutionType**、 **msmErrorBadNullResponse**、 **msmErrorMissingConfigItem** 和 **msmErrorDataRequestFailed**。</span><span class="sxs-lookup"><span data-stu-id="fd8af-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="fd8af-134">這些錯誤會導致合併在遇到錯誤時立即停止。</span><span class="sxs-lookup"><span data-stu-id="fd8af-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="fd8af-135">當 **MergeEx** 傳回 E 失敗時，錯誤物件仍會加入至列舉值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="fd8af-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="fd8af-136">如需有關 msmErrorType 錯誤的詳細資訊，請參閱 [**取得 \_ 型別函數 (Error 物件)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type)。</span><span class="sxs-lookup"><span data-stu-id="fd8af-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="fd8af-137">所有其他錯誤都會導致 **MergeEx** 傳回 \_ FALSE，並導致合併繼續。</span><span class="sxs-lookup"><span data-stu-id="fd8af-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="fd8af-138">C++</span><span class="sxs-lookup"><span data-stu-id="fd8af-138">C++</span></span>

<span data-ttu-id="fd8af-139">請參閱 [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) 函式。</span><span class="sxs-lookup"><span data-stu-id="fd8af-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8af-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd8af-140">Requirements</span></span>



| <span data-ttu-id="fd8af-141">需求</span><span class="sxs-lookup"><span data-stu-id="fd8af-141">Requirement</span></span> | <span data-ttu-id="fd8af-142">值</span><span class="sxs-lookup"><span data-stu-id="fd8af-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8af-143">版本</span><span class="sxs-lookup"><span data-stu-id="fd8af-143">Version</span></span><br/> | <span data-ttu-id="fd8af-144">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fd8af-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="fd8af-145">標頭</span><span class="sxs-lookup"><span data-stu-id="fd8af-145">Header</span></span><br/>  | <dl> <span data-ttu-id="fd8af-146"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8af-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd8af-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fd8af-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd8af-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd8af-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
