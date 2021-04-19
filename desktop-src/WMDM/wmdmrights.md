---
title: WMDMRIGHTS 結構
description: WMDMRIGHTS 結構描述內容使用權利。
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- WMDMRIGHTS 結構 windows Media 裝置管理員
- PWMDMRIGHTS 結構指標 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992798"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="6fbc2-105">WMDMRIGHTS 結構</span><span class="sxs-lookup"><span data-stu-id="6fbc2-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="6fbc2-106">**WMDMRIGHTS** 結構描述內容使用權利。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fbc2-107">語法</span><span class="sxs-lookup"><span data-stu-id="6fbc2-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="6fbc2-108">成員</span><span class="sxs-lookup"><span data-stu-id="6fbc2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fbc2-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6fbc2-111">**dwContentType**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-112">包含內容類型的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="6fbc2-113">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-114">位欄位，指定要用於內容的許可權選項。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="6fbc2-115">值</span><span class="sxs-lookup"><span data-stu-id="6fbc2-115">Value</span></span>                        | <span data-ttu-id="6fbc2-116">描述</span><span class="sxs-lookup"><span data-stu-id="6fbc2-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="6fbc2-117">WMDM \_ RIGHTS \_ PLAYBACKCOUNT</span><span class="sxs-lookup"><span data-stu-id="6fbc2-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="6fbc2-118">檔案可播放的次數。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="6fbc2-119">WMDM \_ RIGHTS \_ EXPIRATIONDATE</span><span class="sxs-lookup"><span data-stu-id="6fbc2-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="6fbc2-120">檔案的到期日。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="6fbc2-121">WMDM \_ RIGHTS \_ FREESERIALIDS</span><span class="sxs-lookup"><span data-stu-id="6fbc2-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="6fbc2-122">檔案的可用串列識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="6fbc2-123">WMDM \_ 許可權 \_ GROUPID 群組</span><span class="sxs-lookup"><span data-stu-id="6fbc2-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="6fbc2-124">檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="6fbc2-125">WMDM \_ RIGHTS \_ NAMEDSERIALIDS</span><span class="sxs-lookup"><span data-stu-id="6fbc2-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="6fbc2-126">檔案的名稱序列識別碼。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="6fbc2-127">**fuRights**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-128">位欄位，包含內容的許可權位。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="6fbc2-129">值</span><span class="sxs-lookup"><span data-stu-id="6fbc2-129">Value</span></span>                                     | <span data-ttu-id="6fbc2-130">描述</span><span class="sxs-lookup"><span data-stu-id="6fbc2-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="6fbc2-131">WMDM \_ 許可權 \_ \_ 在電腦上播放 \_</span><span class="sxs-lookup"><span data-stu-id="6fbc2-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="6fbc2-132">內容可以在個人電腦上播放。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="6fbc2-133">WMDM \_ RIGHTS \_ COPY \_ 至 \_ 非 \_ SDMI \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="6fbc2-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="6fbc2-134">內容可以複製到非 SDMI 裝置。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="6fbc2-135">WMDM \_ 許可權 \_ 複製 \_ 到 \_ CD</span><span class="sxs-lookup"><span data-stu-id="6fbc2-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="6fbc2-136">內容可以複製到 CD。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="6fbc2-137">WMDM \_ 許可權 \_ 複製 \_ 到 \_ SDMI \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="6fbc2-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="6fbc2-138">內容可以複製到 SDMI 裝置。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="6fbc2-139">**dwAppSec**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-140">指定應用程式安全性最小層級的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="6fbc2-141">**dwPlaybackCount**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-142">**DWORD** ，包含內容可轉譯的剩餘時間數。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="6fbc2-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="6fbc2-144">[**WMDMDATETIME**](wmdmdatetime.md) 結構，其中包含內容的到期日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="6fbc2-145">如果授權沒有到期日， **daylightdate.wyear** 成員會設定為0xffff，而 **WMDMDATETIME** 的所有其他成員則會被忽略。</span><span class="sxs-lookup"><span data-stu-id="6fbc2-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fbc2-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fbc2-146">Requirements</span></span>



| <span data-ttu-id="6fbc2-147">需求</span><span class="sxs-lookup"><span data-stu-id="6fbc2-147">Requirement</span></span> | <span data-ttu-id="6fbc2-148">值</span><span class="sxs-lookup"><span data-stu-id="6fbc2-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbc2-149">標頭</span><span class="sxs-lookup"><span data-stu-id="6fbc2-149">Header</span></span><br/> | <dl> <span data-ttu-id="6fbc2-150"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fbc2-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fbc2-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fbc2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbc2-152">**IMDSPStorage::GetRights**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="6fbc2-153">**IWMDMStorage::GetRights**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="6fbc2-154">**WMDMDATETIME**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="6fbc2-155">**結構**</span><span class="sxs-lookup"><span data-stu-id="6fbc2-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





