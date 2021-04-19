---
title: WMDMDATETIME 結構
description: WMDMDATETIME 結構包含一天的日期和時間。
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- WMDMDATETIME 結構 windows Media 裝置管理員
- PWMDMDATETIME 結構指標 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999090"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="daa15-105">WMDMDATETIME 結構</span><span class="sxs-lookup"><span data-stu-id="daa15-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="daa15-106">**WMDMDATETIME** 結構包含一天的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="daa15-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa15-107">語法</span><span class="sxs-lookup"><span data-stu-id="daa15-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="daa15-108">成員</span><span class="sxs-lookup"><span data-stu-id="daa15-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="daa15-109">**Daylightdate.wyear**</span><span class="sxs-lookup"><span data-stu-id="daa15-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="daa15-110">包含四位數年份的單字。</span><span class="sxs-lookup"><span data-stu-id="daa15-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="daa15-111">**wMonth**</span><span class="sxs-lookup"><span data-stu-id="daa15-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="daa15-112">包含月份 (1-12) 的單字。</span><span class="sxs-lookup"><span data-stu-id="daa15-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="daa15-113">**wDay**</span><span class="sxs-lookup"><span data-stu-id="daa15-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="daa15-114">包含當月日期的單字 (1-31) 。</span><span class="sxs-lookup"><span data-stu-id="daa15-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="daa15-115">**wHour**</span><span class="sxs-lookup"><span data-stu-id="daa15-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="daa15-116">包含小時 (0-23) 的單字。</span><span class="sxs-lookup"><span data-stu-id="daa15-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="daa15-117">**wMinute**</span><span class="sxs-lookup"><span data-stu-id="daa15-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="daa15-118">包含分鐘 (0-59) 的單字。</span><span class="sxs-lookup"><span data-stu-id="daa15-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="daa15-119">**wSecond**</span><span class="sxs-lookup"><span data-stu-id="daa15-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="daa15-120">包含第二個 (0-59) 的單字。</span><span class="sxs-lookup"><span data-stu-id="daa15-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="daa15-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="daa15-121">Requirements</span></span>



| <span data-ttu-id="daa15-122">需求</span><span class="sxs-lookup"><span data-stu-id="daa15-122">Requirement</span></span> | <span data-ttu-id="daa15-123">值</span><span class="sxs-lookup"><span data-stu-id="daa15-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="daa15-124">標頭</span><span class="sxs-lookup"><span data-stu-id="daa15-124">Header</span></span><br/> | <dl> <span data-ttu-id="daa15-125"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="daa15-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daa15-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="daa15-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa15-127">**IMDSPStorage：： GetDate**</span><span class="sxs-lookup"><span data-stu-id="daa15-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="daa15-128">**IWMDMStorage：： GetDate**</span><span class="sxs-lookup"><span data-stu-id="daa15-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="daa15-129">**WMDMRIGHTS**</span><span class="sxs-lookup"><span data-stu-id="daa15-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="daa15-130">**結構**</span><span class="sxs-lookup"><span data-stu-id="daa15-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





