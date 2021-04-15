---
title: 'MPSCAN_DATA 結構 (MpClient .h) '
description: 掃描傳遞給回呼的資料。
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA 結構舊版 Windows 環境功能
- PMPSCAN_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466941"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="b8e01-105">MPSCAN \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="b8e01-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="b8e01-106">掃描傳遞給回呼的資料。</span><span class="sxs-lookup"><span data-stu-id="b8e01-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="b8e01-107">此結構包含累計威脅和資源統計資料。</span><span class="sxs-lookup"><span data-stu-id="b8e01-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="b8e01-108">這些 stat 欄位一律有效。</span><span class="sxs-lookup"><span data-stu-id="b8e01-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e01-109">語法</span><span class="sxs-lookup"><span data-stu-id="b8e01-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="b8e01-110">成員</span><span class="sxs-lookup"><span data-stu-id="b8e01-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8e01-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="b8e01-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-112">類型： **[ **MPSCAN \_ 類型**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="b8e01-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8e01-113">掃描類型。</span><span class="sxs-lookup"><span data-stu-id="b8e01-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-114">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="b8e01-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-115">類型： **PMPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b8e01-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="b8e01-116">資源資訊。</span><span class="sxs-lookup"><span data-stu-id="b8e01-116">Resource information.</span></span> <span data-ttu-id="b8e01-117">請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="b8e01-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-118">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="b8e01-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-119">類型： **[ **MPRESOURCE \_ 統計** 資料](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="b8e01-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8e01-120">與資源相關的累計統計資料。</span><span class="sxs-lookup"><span data-stu-id="b8e01-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="b8e01-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="b8e01-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="b8e01-122">類型： **[ **MPTHREAT \_ 統計** 資料](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="b8e01-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b8e01-123">成功完成掃描的威脅統計資料。</span><span class="sxs-lookup"><span data-stu-id="b8e01-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8e01-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8e01-124">Requirements</span></span>



| <span data-ttu-id="b8e01-125">需求</span><span class="sxs-lookup"><span data-stu-id="b8e01-125">Requirement</span></span> | <span data-ttu-id="b8e01-126">值</span><span class="sxs-lookup"><span data-stu-id="b8e01-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e01-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8e01-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e01-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b8e01-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8e01-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e01-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e01-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8e01-131">標頭</span><span class="sxs-lookup"><span data-stu-id="b8e01-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8e01-132"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e01-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e01-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8e01-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e01-134">**MPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="b8e01-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="b8e01-135">**MPRESOURCE \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="b8e01-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="b8e01-136">**MPSCAN \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="b8e01-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="b8e01-137">**MPTHREAT \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="b8e01-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





