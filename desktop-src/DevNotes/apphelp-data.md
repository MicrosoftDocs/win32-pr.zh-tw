---
description: 包含 Apphelp 資料資訊。
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: APPHELP_DATA 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972325"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="b1fa6-103">APPHELP \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="b1fa6-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="b1fa6-104">包含 Apphelp 資料資訊。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1fa6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1fa6-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="b1fa6-106">成員</span><span class="sxs-lookup"><span data-stu-id="b1fa6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1fa6-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-108">這個參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b1fa6-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_停用 \_ 填充碼** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="b1fa6-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_停用 \_ APPHELP** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="b1fa6-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_APPHELP \_ NOUI** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="b1fa6-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_APPHELP \_ 取消** (0x10000000) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="b1fa6-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_停用 \_ SXS** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="b1fa6-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_停用 \_ LAYER** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="b1fa6-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_停用 \_ 驅動程式** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="b1fa6-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b1fa6-116">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-117">此參數可以 APPTYPE \_ 無 (0) 。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-118">**dwHTMLHelpID**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-119">HTML 說明識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-120">**szAppName**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-121">應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-122">**trExe**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-123">對應之可執行檔的 [**TAGREF**](tagref.md) 。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-124">**szURL**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-125">Apphelp online 連結的 URL。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-126">**szLink**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-127">**SzURL** 的連結文字。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-128">**szAppTitle**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-129">Apphelp 訊息的標題。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-130">**szContact**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-131">廠商連絡人資訊。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-132">**szDetails**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-133">詳細的 Apphelp 訊息。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-134">**dwData**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-135">應用程式所管理的使用者定義資料。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="b1fa6-136">**bSPEntry**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="b1fa6-137">如果這個專案是在 service pack 資料庫中，則這個成員為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b1fa6-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1fa6-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1fa6-138">Requirements</span></span>



| <span data-ttu-id="b1fa6-139">需求</span><span class="sxs-lookup"><span data-stu-id="b1fa6-139">Requirement</span></span> | <span data-ttu-id="b1fa6-140">值</span><span class="sxs-lookup"><span data-stu-id="b1fa6-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1fa6-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1fa6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b1fa6-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1fa6-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b1fa6-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1fa6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b1fa6-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1fa6-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1fa6-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1fa6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1fa6-146">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="b1fa6-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




