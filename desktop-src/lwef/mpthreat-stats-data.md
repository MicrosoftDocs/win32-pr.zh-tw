---
title: 'MPTHREAT_STATS_DATA 結構 (MpClient .h) '
description: 其他威脅統計資料資料。
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA 結構舊版 Windows 環境功能
- PMPTHREAT_STATS_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094508"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="c0fca-105">MPTHREAT \_ 統計 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="c0fca-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="c0fca-106">其他威脅統計資料資料。</span><span class="sxs-lookup"><span data-stu-id="c0fca-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0fca-107">語法</span><span class="sxs-lookup"><span data-stu-id="c0fca-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="c0fca-108">成員</span><span class="sxs-lookup"><span data-stu-id="c0fca-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0fca-109">**dwThreatCount**</span><span class="sxs-lookup"><span data-stu-id="c0fca-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="c0fca-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c0fca-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c0fca-111">威脅數目。</span><span class="sxs-lookup"><span data-stu-id="c0fca-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0fca-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0fca-112">Requirements</span></span>



| <span data-ttu-id="c0fca-113">需求</span><span class="sxs-lookup"><span data-stu-id="c0fca-113">Requirement</span></span> | <span data-ttu-id="c0fca-114">值</span><span class="sxs-lookup"><span data-stu-id="c0fca-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fca-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0fca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c0fca-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0fca-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c0fca-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0fca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c0fca-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0fca-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0fca-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c0fca-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0fca-120"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0fca-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





