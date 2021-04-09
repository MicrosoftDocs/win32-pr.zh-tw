---
description: 包含查詢填充碼資料庫以符合可執行檔的結果。
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: SDBQUERYRESULT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936190"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="34cc5-103">SDBQUERYRESULT 結構</span><span class="sxs-lookup"><span data-stu-id="34cc5-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="34cc5-104">包含查詢填充碼資料庫以符合可執行檔的結果。</span><span class="sxs-lookup"><span data-stu-id="34cc5-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="34cc5-105">語法</span><span class="sxs-lookup"><span data-stu-id="34cc5-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="34cc5-106">成員</span><span class="sxs-lookup"><span data-stu-id="34cc5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="34cc5-107">**atrExes**</span><span class="sxs-lookup"><span data-stu-id="34cc5-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-108">相符可執行檔的 **TAGREF** 值。</span><span class="sxs-lookup"><span data-stu-id="34cc5-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="34cc5-109">請注意，「 **SDB \_ 最大 \_ exe** 」定義為16。</span><span class="sxs-lookup"><span data-stu-id="34cc5-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-110">**adwExeFlags**</span><span class="sxs-lookup"><span data-stu-id="34cc5-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-111">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="34cc5-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="34cc5-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_停用 \_ 填充碼** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="34cc5-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_停用 \_ APPHELP** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="34cc5-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_APPHELP \_ NOUI** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="34cc5-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_APPHELP \_ 取消** (0x10000000) </span><span class="sxs-lookup"><span data-stu-id="34cc5-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_停用 \_ SXS** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="34cc5-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_停用 \_ LAYER** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="34cc5-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_停用 \_ 驅動程式** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="34cc5-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="34cc5-119">**atrLayers**</span><span class="sxs-lookup"><span data-stu-id="34cc5-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-120">相符層的 **TAGREF** 值。</span><span class="sxs-lookup"><span data-stu-id="34cc5-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="34cc5-121">請注意，[ **SDB \_ 最大 \_ 層** ] 定義為8。</span><span class="sxs-lookup"><span data-stu-id="34cc5-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-122">**dwLayerFlags**</span><span class="sxs-lookup"><span data-stu-id="34cc5-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-123">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="34cc5-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="34cc5-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_停用 \_ 填充碼** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="34cc5-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_停用 \_ APPHELP** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="34cc5-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_APPHELP \_ NOUI** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="34cc5-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_APPHELP \_ 取消** (0x10000000) </span><span class="sxs-lookup"><span data-stu-id="34cc5-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_停用 \_ SXS** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="34cc5-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_停用 \_ LAYER** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="34cc5-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_停用 \_ 驅動程式** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="34cc5-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="34cc5-131">**trApphelp**</span><span class="sxs-lookup"><span data-stu-id="34cc5-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-132">對應可執行檔之 apphelp 訊息的 **TAGREF** 值。</span><span class="sxs-lookup"><span data-stu-id="34cc5-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-133">**dwExeCount**</span><span class="sxs-lookup"><span data-stu-id="34cc5-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-134">**AtrExes** 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="34cc5-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-135">**dwLayerCount**</span><span class="sxs-lookup"><span data-stu-id="34cc5-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-136">**AtrLayers** 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="34cc5-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-137">**guidID**</span><span class="sxs-lookup"><span data-stu-id="34cc5-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-138">最後一個可執行檔的 GUID。</span><span class="sxs-lookup"><span data-stu-id="34cc5-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="34cc5-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-140">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="34cc5-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="34cc5-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_停用 \_ 填充碼** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="34cc5-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_停用 \_ APPHELP** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="34cc5-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_APPHELP \_ NOUI** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="34cc5-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_APPHELP \_ 取消** (0x10000000) </span><span class="sxs-lookup"><span data-stu-id="34cc5-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_停用 \_ SXS** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="34cc5-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_停用 \_ LAYER** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="34cc5-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="34cc5-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_停用 \_ 驅動程式** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="34cc5-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="34cc5-148">**dwCustomSDBMap**</span><span class="sxs-lookup"><span data-stu-id="34cc5-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-149">自訂填充碼資料庫的對應。</span><span class="sxs-lookup"><span data-stu-id="34cc5-149">A map of the custom shim databases.</span></span> <span data-ttu-id="34cc5-150">如果 **rgGuidDB** 有效，則會設定對應的位。</span><span class="sxs-lookup"><span data-stu-id="34cc5-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="34cc5-151">**rgGuidDB**</span><span class="sxs-lookup"><span data-stu-id="34cc5-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="34cc5-152">填充碼資料庫的 Guid。</span><span class="sxs-lookup"><span data-stu-id="34cc5-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="34cc5-153">請注意，[ **SDB \_ MAX \_ SDBS** ] 定義為16。</span><span class="sxs-lookup"><span data-stu-id="34cc5-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34cc5-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="34cc5-154">Requirements</span></span>



| <span data-ttu-id="34cc5-155">需求</span><span class="sxs-lookup"><span data-stu-id="34cc5-155">Requirement</span></span> | <span data-ttu-id="34cc5-156">值</span><span class="sxs-lookup"><span data-stu-id="34cc5-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="34cc5-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="34cc5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="34cc5-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34cc5-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="34cc5-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="34cc5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="34cc5-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="34cc5-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34cc5-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34cc5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34cc5-162">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="34cc5-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




