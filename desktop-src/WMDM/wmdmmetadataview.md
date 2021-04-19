---
title: WMDMMetadataView 結構
description: WMDMMetadataView 結構定義了元資料檢視。 內容是根據此定義來組織。
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- WMDMMetadataView 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985950"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="7451f-105">WMDMMetadataView 結構</span><span class="sxs-lookup"><span data-stu-id="7451f-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="7451f-106">**WMDMMetadataView** 結構定義了元資料檢視。</span><span class="sxs-lookup"><span data-stu-id="7451f-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="7451f-107">內容是根據此定義來組織。</span><span class="sxs-lookup"><span data-stu-id="7451f-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7451f-108">語法</span><span class="sxs-lookup"><span data-stu-id="7451f-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="7451f-109">成員</span><span class="sxs-lookup"><span data-stu-id="7451f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7451f-110">**pwszViewName**</span><span class="sxs-lookup"><span data-stu-id="7451f-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="7451f-111">寬字元之以 null 結束的字串指標，其中包含視圖名稱。</span><span class="sxs-lookup"><span data-stu-id="7451f-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="7451f-112">這是用來做為顯示這個視圖之根節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="7451f-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="7451f-113">**nDepth**</span><span class="sxs-lookup"><span data-stu-id="7451f-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="7451f-114">包含視圖深度的整數，表示用於視圖的嵌套元資料標記數目。</span><span class="sxs-lookup"><span data-stu-id="7451f-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="7451f-115">**ppwszTags**</span><span class="sxs-lookup"><span data-stu-id="7451f-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="7451f-116">嵌套標記的元資料標記字串陣列。</span><span class="sxs-lookup"><span data-stu-id="7451f-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7451f-117">範例</span><span class="sxs-lookup"><span data-stu-id="7451f-117">Examples</span></span>

<span data-ttu-id="7451f-118">下列程式碼會建立元資料檢視：</span><span class="sxs-lookup"><span data-stu-id="7451f-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="7451f-119">上述程式碼會組織內容，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7451f-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="7451f-120">我的觀點</span><span class="sxs-lookup"><span data-stu-id="7451f-120">My View</span></span><dl> <span data-ttu-id="7451f-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="7451f-121">Genre1</span></span><dl> <span data-ttu-id="7451f-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="7451f-122">Artist1</span></span><dl> <span data-ttu-id="7451f-123">Album1</span><span class="sxs-lookup"><span data-stu-id="7451f-123">Album1</span></span><dl> <span data-ttu-id="7451f-124">Song1</span><span class="sxs-lookup"><span data-stu-id="7451f-124">Song1</span></span>  
<span data-ttu-id="7451f-125">Song2</span><span class="sxs-lookup"><span data-stu-id="7451f-125">Song2</span></span>  
<span data-ttu-id="7451f-126">...</span><span class="sxs-lookup"><span data-stu-id="7451f-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="7451f-127">Album1</span><span class="sxs-lookup"><span data-stu-id="7451f-127">Album1</span></span><dl> <span data-ttu-id="7451f-128">Song1</span><span class="sxs-lookup"><span data-stu-id="7451f-128">Song1</span></span>  
<span data-ttu-id="7451f-129">Song2</span><span class="sxs-lookup"><span data-stu-id="7451f-129">Song2</span></span>  
<span data-ttu-id="7451f-130">...</span><span class="sxs-lookup"><span data-stu-id="7451f-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="7451f-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="7451f-131">Artist1</span></span><dl> <span data-ttu-id="7451f-132">Album1</span><span class="sxs-lookup"><span data-stu-id="7451f-132">Album1</span></span><dl> <span data-ttu-id="7451f-133">Song1</span><span class="sxs-lookup"><span data-stu-id="7451f-133">Song1</span></span>  
<span data-ttu-id="7451f-134">Song2</span><span class="sxs-lookup"><span data-stu-id="7451f-134">Song2</span></span>  
<span data-ttu-id="7451f-135">...</span><span class="sxs-lookup"><span data-stu-id="7451f-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="7451f-136">Album1</span><span class="sxs-lookup"><span data-stu-id="7451f-136">Album1</span></span><dl> <span data-ttu-id="7451f-137">Song1</span><span class="sxs-lookup"><span data-stu-id="7451f-137">Song1</span></span>  
<span data-ttu-id="7451f-138">Song2</span><span class="sxs-lookup"><span data-stu-id="7451f-138">Song2</span></span>  
<span data-ttu-id="7451f-139">...</span><span class="sxs-lookup"><span data-stu-id="7451f-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7451f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="7451f-140">Requirements</span></span>



| <span data-ttu-id="7451f-141">需求</span><span class="sxs-lookup"><span data-stu-id="7451f-141">Requirement</span></span> | <span data-ttu-id="7451f-142">值</span><span class="sxs-lookup"><span data-stu-id="7451f-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7451f-143">標頭</span><span class="sxs-lookup"><span data-stu-id="7451f-143">Header</span></span><br/> | <dl> <span data-ttu-id="7451f-144"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7451f-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7451f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7451f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7451f-146">**結構**</span><span class="sxs-lookup"><span data-stu-id="7451f-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





