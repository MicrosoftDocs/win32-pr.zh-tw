---
title: 'SwarmStatus 列舉 (>deliveryoptimization) '
description: 定義傳遞優化用戶端內檔案的狀態。
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- SwarmStatus 列舉
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105318"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="8b779-104">SwarmStatus 列舉</span><span class="sxs-lookup"><span data-stu-id="8b779-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="8b779-105">定義傳遞優化用戶端內檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="8b779-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b779-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b779-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="8b779-107">常數</span><span class="sxs-lookup"><span data-stu-id="8b779-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8b779-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="8b779-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="8b779-109">正在下載檔案。</span><span class="sxs-lookup"><span data-stu-id="8b779-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="8b779-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="8b779-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="8b779-111">檔案下載已完成。</span><span class="sxs-lookup"><span data-stu-id="8b779-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="8b779-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="8b779-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="8b779-113">檔案正在進行快取。</span><span class="sxs-lookup"><span data-stu-id="8b779-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="8b779-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="8b779-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="8b779-115">檔案下載已暫停。</span><span class="sxs-lookup"><span data-stu-id="8b779-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b779-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b779-116">Requirements</span></span>



| <span data-ttu-id="8b779-117">需求</span><span class="sxs-lookup"><span data-stu-id="8b779-117">Requirement</span></span> | <span data-ttu-id="8b779-118">值</span><span class="sxs-lookup"><span data-stu-id="8b779-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b779-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b779-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b779-120">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b779-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b779-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b779-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b779-122">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b779-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b779-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8b779-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b779-124"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b779-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





