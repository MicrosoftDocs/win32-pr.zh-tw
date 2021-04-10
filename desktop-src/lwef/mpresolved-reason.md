---
title: 'MPRESOLVED_REASON 列舉 (MpClient .h) '
description: 解決補救失敗的可能原因。
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON 列舉舊版 Windows 環境功能
- PMPRESOLVED_REASON 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025261"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="a3bdb-105">MPRESOLVED \_ 原因列舉</span><span class="sxs-lookup"><span data-stu-id="a3bdb-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="a3bdb-106">解決補救失敗的可能原因。</span><span class="sxs-lookup"><span data-stu-id="a3bdb-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bdb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3bdb-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="a3bdb-108">常數</span><span class="sxs-lookup"><span data-stu-id="a3bdb-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a3bdb-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**未知的 MPRESOLVED \_ 原因 \_**</span><span class="sxs-lookup"><span data-stu-id="a3bdb-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="a3bdb-110">處於錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="a3bdb-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="a3bdb-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED \_ 原因 \_ 完整 \_ 掃描**</span><span class="sxs-lookup"><span data-stu-id="a3bdb-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="a3bdb-112">已執行完整掃描。</span><span class="sxs-lookup"><span data-stu-id="a3bdb-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="a3bdb-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED \_ 原因已 \_ 超時 \_**</span><span class="sxs-lookup"><span data-stu-id="a3bdb-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="a3bdb-114">經過的時間已足夠。</span><span class="sxs-lookup"><span data-stu-id="a3bdb-114">Enough time has passed.</span></span> <span data-ttu-id="a3bdb-115">預設值為一周。</span><span class="sxs-lookup"><span data-stu-id="a3bdb-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3bdb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3bdb-116">Requirements</span></span>



| <span data-ttu-id="a3bdb-117">需求</span><span class="sxs-lookup"><span data-stu-id="a3bdb-117">Requirement</span></span> | <span data-ttu-id="a3bdb-118">值</span><span class="sxs-lookup"><span data-stu-id="a3bdb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bdb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3bdb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a3bdb-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3bdb-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a3bdb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3bdb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a3bdb-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3bdb-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3bdb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a3bdb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3bdb-124"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3bdb-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





