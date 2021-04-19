---
description: Merge 物件的 CreateSourceImage 方法可讓用戶端在合併後將模組中的檔案解壓縮到磁片上的來源影像，並將變更模組設定期間可能進行的模組變更納入考慮。
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: 'CreateSourceImage 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990205"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="c6052-103">Merge. CreateSourceImage 方法</span><span class="sxs-lookup"><span data-stu-id="c6052-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="c6052-104">[**Merge**](merge-object.md)物件的 **CreateSourceImage** 方法可讓用戶端在合併後將模組中的檔案解壓縮到磁片上的來源影像，並將變更模組設定期間可能進行的模組變更納入考慮。</span><span class="sxs-lookup"><span data-stu-id="c6052-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="c6052-105">合併處理期間，會從模組的檔案資料表中取出要解壓縮的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="c6052-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="c6052-106">檔案清單是由從模組的檔案資料表成功複製到目標資料庫的每個檔案所組成。</span><span class="sxs-lookup"><span data-stu-id="c6052-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="c6052-107">由於主鍵與資料庫中現有的資料列衝突，所以未複製的檔案資料表專案不是此清單的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6052-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="c6052-108">在建立映射時，這些檔案的每個目錄都是來自開啟的 (後置合併) 資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6052-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="c6052-109">*Path* 參數中指定的路徑是安裝來源映射的根目錄。</span><span class="sxs-lookup"><span data-stu-id="c6052-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="c6052-110">*fLongFileNames* 會判斷路徑區段和最終檔案名是否使用長檔名。</span><span class="sxs-lookup"><span data-stu-id="c6052-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="c6052-111">如果沒有開啟任何資料庫、未開啟任何模組，或尚未執行任何合併，則函數會失敗。</span><span class="sxs-lookup"><span data-stu-id="c6052-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6052-112">語法</span><span class="sxs-lookup"><span data-stu-id="c6052-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="c6052-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6052-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6052-114">*路徑*</span><span class="sxs-lookup"><span data-stu-id="c6052-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="c6052-115">要安裝之來源映射的根目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="c6052-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="c6052-116">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="c6052-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="c6052-117">*fLongFileNames* 會判斷路徑區段和最終檔案名是否使用長檔名。</span><span class="sxs-lookup"><span data-stu-id="c6052-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="c6052-118">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="c6052-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="c6052-119">這是已成功解壓縮之檔案的完整路徑清單。</span><span class="sxs-lookup"><span data-stu-id="c6052-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6052-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6052-120">Return value</span></span>

<span data-ttu-id="c6052-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c6052-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6052-122">備註</span><span class="sxs-lookup"><span data-stu-id="c6052-122">Remarks</span></span>

<span data-ttu-id="c6052-123">目的地目錄中具有相同名稱的任何檔案都會遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="c6052-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="c6052-124">如果路徑不存在，則會建立路徑。</span><span class="sxs-lookup"><span data-stu-id="c6052-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="c6052-125">C++</span><span class="sxs-lookup"><span data-stu-id="c6052-125">C++</span></span>

<span data-ttu-id="c6052-126">請參閱 [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) 函式。</span><span class="sxs-lookup"><span data-stu-id="c6052-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6052-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6052-127">Requirements</span></span>



| <span data-ttu-id="c6052-128">需求</span><span class="sxs-lookup"><span data-stu-id="c6052-128">Requirement</span></span> | <span data-ttu-id="c6052-129">值</span><span class="sxs-lookup"><span data-stu-id="c6052-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6052-130">版本</span><span class="sxs-lookup"><span data-stu-id="c6052-130">Version</span></span><br/> | <span data-ttu-id="c6052-131">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c6052-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c6052-132">標頭</span><span class="sxs-lookup"><span data-stu-id="c6052-132">Header</span></span><br/>  | <dl> <span data-ttu-id="c6052-133"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6052-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6052-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c6052-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6052-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6052-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




