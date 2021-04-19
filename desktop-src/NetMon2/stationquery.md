---
description: STATIONQUERY 結構會使用網路監視器來提供特定電腦的相關資訊。
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: 'STATIONQUERY 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997516"
---
# <a name="stationquery-structure"></a><span data-ttu-id="d5513-103">STATIONQUERY 結構</span><span class="sxs-lookup"><span data-stu-id="d5513-103">STATIONQUERY structure</span></span>

<span data-ttu-id="d5513-104">**STATIONQUERY** 結構會使用網路監視器來提供特定電腦的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d5513-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5513-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5513-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="d5513-106">成員</span><span class="sxs-lookup"><span data-stu-id="d5513-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5513-107">**旗標**</span><span class="sxs-lookup"><span data-stu-id="d5513-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-108">識別網路監視器目前狀態的旗標。</span><span class="sxs-lookup"><span data-stu-id="d5513-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="d5513-109">值</span><span class="sxs-lookup"><span data-stu-id="d5513-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="d5513-110">意義</span><span class="sxs-lookup"><span data-stu-id="d5513-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="d5513-111"><dt>**已 \_ 載入 STATIONQUERY 旗標 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5513-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="d5513-112">驅動程式已載入，但核心不是。</span><span class="sxs-lookup"><span data-stu-id="d5513-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="d5513-113"><dt>**STATIONQUERY \_ 旗標 \_ 正在執行**</dt></span><span class="sxs-lookup"><span data-stu-id="d5513-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="d5513-114">驅動程式已載入，但未捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="d5513-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="d5513-115"><dt>**STATIONQUERY \_ 旗標 \_ 捕獲**</dt></span><span class="sxs-lookup"><span data-stu-id="d5513-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="d5513-116">驅動程式積極參與捕捉。</span><span class="sxs-lookup"><span data-stu-id="d5513-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="d5513-117"><dt>**STATIONQUERY \_ 旗標 \_ 傳輸**</dt></span><span class="sxs-lookup"><span data-stu-id="d5513-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="d5513-118">這個旗標已過時。</span><span class="sxs-lookup"><span data-stu-id="d5513-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="d5513-119">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="d5513-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-120">電腦上安裝網路監視器的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d5513-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-121">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="d5513-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-122">電腦上安裝網路監視器的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d5513-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-123">**LicenseNumber**</span><span class="sxs-lookup"><span data-stu-id="d5513-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-124">軟體授權號碼。</span><span class="sxs-lookup"><span data-stu-id="d5513-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="d5513-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-126">電腦製造商名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d5513-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-127">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="d5513-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-128">使用者名稱或系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5513-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-129">**已保留**</span><span class="sxs-lookup"><span data-stu-id="d5513-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-130">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="d5513-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-131">**AdapterAddress**</span><span class="sxs-lookup"><span data-stu-id="d5513-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-132">NIC 位址。</span><span class="sxs-lookup"><span data-stu-id="d5513-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-133">**WMachineName**</span><span class="sxs-lookup"><span data-stu-id="d5513-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-134">Unicode 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="d5513-134">Unicode computer name.</span></span> <span data-ttu-id="d5513-135">此成員適用于網路監視器2.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d5513-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="d5513-136">**WUserName**</span><span class="sxs-lookup"><span data-stu-id="d5513-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="d5513-137">Unicode 使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d5513-137">Unicode user name.</span></span> <span data-ttu-id="d5513-138">此成員適用于網路監視器2.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d5513-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5513-139">備註</span><span class="sxs-lookup"><span data-stu-id="d5513-139">Remarks</span></span>

<span data-ttu-id="d5513-140">資料表資料表會使用 [這些結構的](querytable.md) 陣列來提供目前使用網路監視器來捕捉資料的電腦清單。</span><span class="sxs-lookup"><span data-stu-id="d5513-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5513-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5513-141">Requirements</span></span>



| <span data-ttu-id="d5513-142">需求</span><span class="sxs-lookup"><span data-stu-id="d5513-142">Requirement</span></span> | <span data-ttu-id="d5513-143">值</span><span class="sxs-lookup"><span data-stu-id="d5513-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d5513-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5513-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d5513-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5513-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d5513-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5513-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d5513-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5513-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d5513-148">標頭</span><span class="sxs-lookup"><span data-stu-id="d5513-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5513-149"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d5513-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5513-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5513-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5513-151">透視</span><span class="sxs-lookup"><span data-stu-id="d5513-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 




