---
description: Merge 物件的 ExtractFiles 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: 'ExtractFiles 方法 (Advpub .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997693"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="b01b2-103">Merge. ExtractFiles 方法</span><span class="sxs-lookup"><span data-stu-id="b01b2-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="b01b2-104">[**Merge**](merge-object.md)物件的 **ExtractFiles** 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="b01b2-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="b01b2-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="b01b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="b01b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b01b2-107">*路徑*</span><span class="sxs-lookup"><span data-stu-id="b01b2-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="b01b2-108">完整的目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="b01b2-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b01b2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b01b2-109">Return value</span></span>

<span data-ttu-id="b01b2-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b01b2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b01b2-111">備註</span><span class="sxs-lookup"><span data-stu-id="b01b2-111">Remarks</span></span>

<span data-ttu-id="b01b2-112">目的地目錄中具有相同名稱的任何檔案都會遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="b01b2-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="b01b2-113">如果路徑不存在，則會建立路徑。</span><span class="sxs-lookup"><span data-stu-id="b01b2-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="b01b2-114">**ExtractFiles** 一律會使用路徑的簡短檔案名來解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="b01b2-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="b01b2-115">若要針對路徑使用長檔名，請使用 [**ExtractFilesEx 方法**](merge-extractfilesex.md)。</span><span class="sxs-lookup"><span data-stu-id="b01b2-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="b01b2-116">C++</span><span class="sxs-lookup"><span data-stu-id="b01b2-116">C++</span></span>

<span data-ttu-id="b01b2-117">請參閱 [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) 函式。</span><span class="sxs-lookup"><span data-stu-id="b01b2-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01b2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b01b2-118">Requirements</span></span>



| <span data-ttu-id="b01b2-119">需求</span><span class="sxs-lookup"><span data-stu-id="b01b2-119">Requirement</span></span> | <span data-ttu-id="b01b2-120">值</span><span class="sxs-lookup"><span data-stu-id="b01b2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b01b2-121">版本</span><span class="sxs-lookup"><span data-stu-id="b01b2-121">Version</span></span><br/> | <span data-ttu-id="b01b2-122">Mergemod.dll 1.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b01b2-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="b01b2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b01b2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b01b2-124"><dt>Advpub (包含 Mergemod) </dt></span><span class="sxs-lookup"><span data-stu-id="b01b2-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="b01b2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b01b2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b01b2-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01b2-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
