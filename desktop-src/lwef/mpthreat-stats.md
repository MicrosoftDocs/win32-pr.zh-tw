---
title: 'MPTHREAT_STATS 結構 (MpClient .h) '
description: 威脅相關的統計資料。
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS 結構舊版 Windows 環境功能
- PMPTHREAT_STATS 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843500"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="c3539-105">MPTHREAT \_ 統計結構</span><span class="sxs-lookup"><span data-stu-id="c3539-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="c3539-106">威脅相關的統計資料。</span><span class="sxs-lookup"><span data-stu-id="c3539-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3539-107">語法</span><span class="sxs-lookup"><span data-stu-id="c3539-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="c3539-108">成員</span><span class="sxs-lookup"><span data-stu-id="c3539-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3539-109">**ThreatCount**</span><span class="sxs-lookup"><span data-stu-id="c3539-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="c3539-110">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="c3539-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="c3539-111">偵測到的威脅數目。</span><span class="sxs-lookup"><span data-stu-id="c3539-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="c3539-112">**SuspiciousThreatCount**</span><span class="sxs-lookup"><span data-stu-id="c3539-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="c3539-113">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="c3539-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="c3539-114">使用行為監視偵測到的威脅數目。</span><span class="sxs-lookup"><span data-stu-id="c3539-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="c3539-115">**已保留**</span><span class="sxs-lookup"><span data-stu-id="c3539-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c3539-116">類型： **UINT \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="c3539-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="c3539-117">保留供日後使用的欄位。</span><span class="sxs-lookup"><span data-stu-id="c3539-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3539-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3539-118">Requirements</span></span>



| <span data-ttu-id="c3539-119">需求</span><span class="sxs-lookup"><span data-stu-id="c3539-119">Requirement</span></span> | <span data-ttu-id="c3539-120">值</span><span class="sxs-lookup"><span data-stu-id="c3539-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3539-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c3539-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3539-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3539-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c3539-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c3539-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3539-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c3539-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3539-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c3539-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3539-126"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3539-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





