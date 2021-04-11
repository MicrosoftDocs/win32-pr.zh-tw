---
description: 監視器 \_ 資訊 \_ 2 結構會識別監視。
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: 'MONITOR_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695079"
---
# <a name="monitor_info_2-structure"></a><span data-ttu-id="7c22c-103">監視 \_ INFO \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="7c22c-103">MONITOR\_INFO\_2 structure</span></span>

<span data-ttu-id="7c22c-104">**監視器 \_ 資訊 \_ 2** 結構會識別監視。</span><span class="sxs-lookup"><span data-stu-id="7c22c-104">The **MONITOR\_INFO\_2** structure identifies a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c22c-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c22c-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="7c22c-106">成員</span><span class="sxs-lookup"><span data-stu-id="7c22c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c22c-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="7c22c-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="7c22c-108">以 null 結束的字串指標，也就是監視的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c22c-108">A pointer to a null-terminated string that is the name of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7c22c-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="7c22c-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="7c22c-110">以 null 結束的字串指標，可指定用來寫入監視器的環境 (例如 Windows NT x86、Windows IA64、Windows x64) 。</span><span class="sxs-lookup"><span data-stu-id="7c22c-110">A pointer to a null-terminated string that specifies the environment for which the monitor was written (for example, Windows NT x86, Windows IA64, Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="7c22c-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="7c22c-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="7c22c-112">以 null 結束的字串指標，該字串為監視器 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c22c-112">A pointer to a null-terminated string that is the name of the monitor DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c22c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c22c-113">Requirements</span></span>



| <span data-ttu-id="7c22c-114">需求</span><span class="sxs-lookup"><span data-stu-id="7c22c-114">Requirement</span></span> | <span data-ttu-id="7c22c-115">值</span><span class="sxs-lookup"><span data-stu-id="7c22c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c22c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c22c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7c22c-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c22c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c22c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c22c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7c22c-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c22c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c22c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7c22c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c22c-121"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7c22c-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7c22c-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="7c22c-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7c22c-123">**\_ 監視器 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 監視 \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="7c22c-123">**\_MONITOR\_INFO\_2W** (Unicode) and **\_MONITOR\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="7c22c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c22c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c22c-125">列印</span><span class="sxs-lookup"><span data-stu-id="7c22c-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7c22c-126">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="7c22c-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7c22c-127">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="7c22c-127">**AddMonitor**</span></span>](addmonitor.md)
</dt> <dt>

[<span data-ttu-id="7c22c-128">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="7c22c-128">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="7c22c-129">**監視 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="7c22c-129">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> </dl>

 

 




