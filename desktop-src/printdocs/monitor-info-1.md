---
description: 監視器 \_ 資訊 \_ 1 結構會識別已安裝的監視器。
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: 'MONITOR_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6af1e1b9111ac6221273f2faf68fc6ed70e07a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001367"
---
# <a name="monitor_info_1-structure"></a><span data-ttu-id="8dfbb-103">監視 \_ 資訊 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="8dfbb-103">MONITOR\_INFO\_1 structure</span></span>

<span data-ttu-id="8dfbb-104">**監視器 \_ 資訊 \_ 1** 結構會識別已安裝的監視器。</span><span class="sxs-lookup"><span data-stu-id="8dfbb-104">The **MONITOR\_INFO\_1** structure identifies an installed monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfbb-105">語法</span><span class="sxs-lookup"><span data-stu-id="8dfbb-105">Syntax</span></span>


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="8dfbb-106">成員</span><span class="sxs-lookup"><span data-stu-id="8dfbb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8dfbb-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="8dfbb-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="8dfbb-108">識別已安裝監視器之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="8dfbb-108">A pointer to a null-terminated string that identifies an installed monitor.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dfbb-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dfbb-109">Requirements</span></span>



| <span data-ttu-id="8dfbb-110">需求</span><span class="sxs-lookup"><span data-stu-id="8dfbb-110">Requirement</span></span> | <span data-ttu-id="8dfbb-111">值</span><span class="sxs-lookup"><span data-stu-id="8dfbb-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfbb-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8dfbb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfbb-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8dfbb-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8dfbb-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8dfbb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfbb-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8dfbb-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8dfbb-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8dfbb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dfbb-117"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8dfbb-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8dfbb-118">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="8dfbb-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8dfbb-119">**\_ 監視 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 監視 \_ 資訊 \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="8dfbb-119">**\_MONITOR\_INFO\_1W** (Unicode) and **\_MONITOR\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="8dfbb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dfbb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfbb-121">列印</span><span class="sxs-lookup"><span data-stu-id="8dfbb-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8dfbb-122">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="8dfbb-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8dfbb-123">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="8dfbb-123">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="8dfbb-124">**監視 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8dfbb-124">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

 




