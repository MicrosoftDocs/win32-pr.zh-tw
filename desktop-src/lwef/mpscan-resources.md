---
title: 'MPSCAN_RESOURCES 結構 (MpClient .h) '
description: 掃描操作期間傳遞的資源資訊。
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES 結構舊版 Windows 環境功能
- PMPSCAN_RESOURCES 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935103"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="70fae-105">MPSCAN \_ 資源結構</span><span class="sxs-lookup"><span data-stu-id="70fae-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="70fae-106">掃描操作期間傳遞的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="70fae-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="70fae-107">語法</span><span class="sxs-lookup"><span data-stu-id="70fae-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="70fae-108">成員</span><span class="sxs-lookup"><span data-stu-id="70fae-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70fae-109">**dwResourceCount**</span><span class="sxs-lookup"><span data-stu-id="70fae-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="70fae-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="70fae-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="70fae-111">資源計數。</span><span class="sxs-lookup"><span data-stu-id="70fae-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="70fae-112">**pResourceList**</span><span class="sxs-lookup"><span data-stu-id="70fae-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="70fae-113">類型： **PMPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="70fae-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="70fae-114">資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="70fae-114">Array of resources.</span></span> <span data-ttu-id="70fae-115">請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="70fae-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70fae-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="70fae-116">Requirements</span></span>



| <span data-ttu-id="70fae-117">需求</span><span class="sxs-lookup"><span data-stu-id="70fae-117">Requirement</span></span> | <span data-ttu-id="70fae-118">值</span><span class="sxs-lookup"><span data-stu-id="70fae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70fae-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70fae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70fae-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70fae-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="70fae-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70fae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70fae-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70fae-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70fae-123">標頭</span><span class="sxs-lookup"><span data-stu-id="70fae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="70fae-124"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="70fae-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70fae-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70fae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70fae-126">**MPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="70fae-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





