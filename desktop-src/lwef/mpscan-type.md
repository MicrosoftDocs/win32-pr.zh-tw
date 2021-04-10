---
title: 'MPSCAN_TYPE 列舉 (MpClient .h) '
description: 執行的掃描類型。
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE 列舉舊版 Windows 環境功能
- PMPSCAN_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685566"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="d5d39-105">MPSCAN \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="d5d39-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="d5d39-106">執行的掃描類型。</span><span class="sxs-lookup"><span data-stu-id="d5d39-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d39-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5d39-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d5d39-108">常數</span><span class="sxs-lookup"><span data-stu-id="d5d39-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d5d39-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**未知的 MPSCAN \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="d5d39-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="d5d39-110">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="d5d39-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="d5d39-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ 類型 \_ 快速**</span><span class="sxs-lookup"><span data-stu-id="d5d39-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="d5d39-112">掃描執行中的進程，以及惡意程式碼通常隱藏在系統中的各種 ASEP 點。</span><span class="sxs-lookup"><span data-stu-id="d5d39-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="d5d39-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN \_ 類型 \_ FULL**</span><span class="sxs-lookup"><span data-stu-id="d5d39-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="d5d39-114">執行快速掃描，然後掃描系統的所有固定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d5d39-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5d39-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN \_ 類型 \_ 資源**</span><span class="sxs-lookup"><span data-stu-id="d5d39-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="d5d39-116">掃描特定的資源，例如檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="d5d39-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="d5d39-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN \_ 類型 \_**</span><span class="sxs-lookup"><span data-stu-id="d5d39-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="d5d39-118">可能的最大值。</span><span class="sxs-lookup"><span data-stu-id="d5d39-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5d39-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5d39-119">Requirements</span></span>



| <span data-ttu-id="d5d39-120">需求</span><span class="sxs-lookup"><span data-stu-id="d5d39-120">Requirement</span></span> | <span data-ttu-id="d5d39-121">值</span><span class="sxs-lookup"><span data-stu-id="d5d39-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d39-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5d39-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d39-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5d39-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d5d39-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5d39-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d39-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5d39-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5d39-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d5d39-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5d39-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d39-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





