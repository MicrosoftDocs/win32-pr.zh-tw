---
description: 用來處理 DirectX. x 檔案的方法除了標準的 COM 傳回值之外，還可以傳回下列值。 已取代。
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: '傳回值 (DXFile) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696699"
---
# <a name="return-values-dxfileh"></a><span data-ttu-id="d34e0-104">傳回值 (DXFile) </span><span class="sxs-lookup"><span data-stu-id="d34e0-104">Return Values (DXFile.h)</span></span>

<span data-ttu-id="d34e0-105">用來處理 DirectX. x 檔案的方法除了標準的 COM 傳回值之外，還可以傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="d34e0-105">The methods used to work with DirectX .x files can return the following values in addition to the standard COM return values.</span></span> <span data-ttu-id="d34e0-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="d34e0-106">Deprecated.</span></span>

<dl> <dt>

<span data-ttu-id="d34e0-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ 確定**</span><span class="sxs-lookup"><span data-stu-id="d34e0-107"><span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-108">命令已順利完成。</span><span class="sxs-lookup"><span data-stu-id="d34e0-108">Command completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR \_ BADALLOC**</span><span class="sxs-lookup"><span data-stu-id="d34e0-109"><span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR\_BADALLOC**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-110">記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="d34e0-110">Memory allocation failed.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR \_ BADARRAYSIZE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-111"><span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR\_BADARRAYSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-112">陣列大小無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-112">Array size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR \_ BADCACHEFILE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-113"><span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR\_BADCACHEFILE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-114">包含. x 檔案日期的快取檔案無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-114">The cache file containing the .x file date is invalid.</span></span> <span data-ttu-id="d34e0-115">快取檔案包含從網路抓取、在硬碟上快取，並在後續要求中取出的資料。</span><span class="sxs-lookup"><span data-stu-id="d34e0-115">A cache file contains data retrieved from the network, cached on the hard disk, and retrieved in subsequent requests.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR \_ BADDataReference**</span><span class="sxs-lookup"><span data-stu-id="d34e0-116"><span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR\_BADDataReference**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-117">資料參考無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-117">Data reference is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR \_ BADFILE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-118"><span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR\_BADFILE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-119">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-119">File is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR \_ BADFILECOMPRESSIONTYPE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-120"><span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR\_BADFILECOMPRESSIONTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-121">檔案壓縮類型無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-121">File compression type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR \_ BADFILEFLOATSIZE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-122"><span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR\_BADFILEFLOATSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-123">浮點數大小無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-123">Floating-point size is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR \_ BADFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-124"><span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR\_BADFILETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-125">檔案不是 DirectX. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="d34e0-125">File is not a DirectX .x file.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR \_ BADFILEVERSION**</span><span class="sxs-lookup"><span data-stu-id="d34e0-126"><span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR\_BADFILEVERSION**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-127">檔案版本無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-127">File version is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR \_ BADINTRINSICS**</span><span class="sxs-lookup"><span data-stu-id="d34e0-128"><span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR\_BADINTRINSICS**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-129">內建函式無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-129">Intrinsics are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR \_ BADOBJECT**</span><span class="sxs-lookup"><span data-stu-id="d34e0-130"><span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR\_BADOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-131">無效的物件。</span><span class="sxs-lookup"><span data-stu-id="d34e0-131">Object is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR \_ BADRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-132"><span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR\_BADRESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-133">資源無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-133">Resource is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR \_ BADSTREAMHANDLE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-134"><span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR\_BADSTREAMHANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-135">資料流程控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-135">Stream handle is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR \_ BADTYPE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-136"><span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR\_BADTYPE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-137">物件類型無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-137">Object type is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR \_ BADVALUE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-138"><span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR\_BADVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-139">參數無效。</span><span class="sxs-lookup"><span data-stu-id="d34e0-139">Parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR \_ FILENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="d34e0-140"><span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR\_FILENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-141">找不到檔案。</span><span class="sxs-lookup"><span data-stu-id="d34e0-141">File could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="d34e0-142"><span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR\_INTERNALERROR**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-143">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="d34e0-143">Internal error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOINTERNET**</span><span class="sxs-lookup"><span data-stu-id="d34e0-144"><span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR\_NOINTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-145">找不到網際網路連接。</span><span class="sxs-lookup"><span data-stu-id="d34e0-145">Internet connection not found.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR \_ NOMOREDATA**</span><span class="sxs-lookup"><span data-stu-id="d34e0-146"><span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR\_NOMOREDATA**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-147">沒有其他資料可供使用。</span><span class="sxs-lookup"><span data-stu-id="d34e0-147">No further data is available.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR \_ NOMOREOBJECTS**</span><span class="sxs-lookup"><span data-stu-id="d34e0-148"><span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR\_NOMOREOBJECTS**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-149">所有物件都已列舉。</span><span class="sxs-lookup"><span data-stu-id="d34e0-149">All objects have been enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR \_ NOMORESTREAMHANDLES**</span><span class="sxs-lookup"><span data-stu-id="d34e0-150"><span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR\_NOMORESTREAMHANDLES**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-151">未提供任何資料流程控制碼。</span><span class="sxs-lookup"><span data-stu-id="d34e0-151">No stream handles are available.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR \_ NOTDONEYET**</span><span class="sxs-lookup"><span data-stu-id="d34e0-152"><span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR\_NOTDONEYET**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-153">作業尚未完成。</span><span class="sxs-lookup"><span data-stu-id="d34e0-153">Operation has not completed.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR \_ NOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="d34e0-154"><span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR\_NOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-155">找不到物件。</span><span class="sxs-lookup"><span data-stu-id="d34e0-155">Object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR \_ PARSEERROR**</span><span class="sxs-lookup"><span data-stu-id="d34e0-156"><span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR\_PARSEERROR**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-157">無法剖析檔案。</span><span class="sxs-lookup"><span data-stu-id="d34e0-157">File could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR \_ RESOURCENOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="d34e0-158"><span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR\_RESOURCENOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-159">找不到資源。</span><span class="sxs-lookup"><span data-stu-id="d34e0-159">Resource could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR \_ NOTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="d34e0-160"><span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR\_NOTEMPLATE**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-161">沒有任何可用的範本。</span><span class="sxs-lookup"><span data-stu-id="d34e0-161">No template available.</span></span>

</dd> <dt>

<span data-ttu-id="d34e0-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR \_ URLNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="d34e0-162"><span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR\_URLNOTFOUND**</span></span>
</dt> <dd>

<span data-ttu-id="d34e0-163">找不到 URL。</span><span class="sxs-lookup"><span data-stu-id="d34e0-163">URL could not be found.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d34e0-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="d34e0-164">Requirements</span></span>



| <span data-ttu-id="d34e0-165">需求</span><span class="sxs-lookup"><span data-stu-id="d34e0-165">Requirement</span></span> | <span data-ttu-id="d34e0-166">值</span><span class="sxs-lookup"><span data-stu-id="d34e0-166">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d34e0-167">標頭</span><span class="sxs-lookup"><span data-stu-id="d34e0-167">Header</span></span><br/> | <dl> <span data-ttu-id="d34e0-168"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="d34e0-168"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d34e0-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d34e0-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34e0-170"> (舊版) 的 X 檔案參考 </span><span class="sxs-lookup"><span data-stu-id="d34e0-170">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




