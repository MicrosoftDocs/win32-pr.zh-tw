---
description: Merge 物件的 ExtractFilesEx 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: 'ExtractFilesEx 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995492"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="9c183-103">Merge. ExtractFilesEx 方法</span><span class="sxs-lookup"><span data-stu-id="9c183-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="9c183-104">[**Merge**](merge-object.md)物件的 **ExtractFilesEx** 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="9c183-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c183-105">語法</span><span class="sxs-lookup"><span data-stu-id="9c183-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="9c183-106">參數</span><span class="sxs-lookup"><span data-stu-id="9c183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c183-107">*路徑*</span><span class="sxs-lookup"><span data-stu-id="9c183-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="9c183-108">完整的目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="9c183-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="9c183-109">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="9c183-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="9c183-110">設定為使用路徑區段和最終檔案名的完整檔案名來指定。</span><span class="sxs-lookup"><span data-stu-id="9c183-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="9c183-111">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="9c183-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="9c183-112">這是已成功解壓縮之檔案的完整路徑清單。</span><span class="sxs-lookup"><span data-stu-id="9c183-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c183-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c183-113">Return value</span></span>

<span data-ttu-id="9c183-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c183-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c183-115">備註</span><span class="sxs-lookup"><span data-stu-id="9c183-115">Remarks</span></span>

<span data-ttu-id="9c183-116">目的地目錄中具有相同名稱的任何檔案都會遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="9c183-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="9c183-117">如果路徑不存在，則會建立路徑。</span><span class="sxs-lookup"><span data-stu-id="9c183-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="9c183-118">C++</span><span class="sxs-lookup"><span data-stu-id="9c183-118">C++</span></span>

<span data-ttu-id="9c183-119">請參閱 [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) 函式。</span><span class="sxs-lookup"><span data-stu-id="9c183-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c183-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c183-120">Requirements</span></span>



| <span data-ttu-id="9c183-121">需求</span><span class="sxs-lookup"><span data-stu-id="9c183-121">Requirement</span></span> | <span data-ttu-id="9c183-122">值</span><span class="sxs-lookup"><span data-stu-id="9c183-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c183-123">版本</span><span class="sxs-lookup"><span data-stu-id="9c183-123">Version</span></span><br/> | <span data-ttu-id="9c183-124">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9c183-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="9c183-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9c183-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9c183-126"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="9c183-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c183-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9c183-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="9c183-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c183-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




