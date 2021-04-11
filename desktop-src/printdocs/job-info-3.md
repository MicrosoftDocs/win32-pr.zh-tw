---
description: 作業 \_ 資訊 \_ 3 結構是用來將一組列印工作連結在一起。
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: 'JOB_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194962"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="b2522-103">作業 \_ 資訊 \_ 3 結構</span><span class="sxs-lookup"><span data-stu-id="b2522-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="b2522-104">**作業 \_ 資訊 \_ 3** 結構是用來將一組列印工作連結在一起。</span><span class="sxs-lookup"><span data-stu-id="b2522-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2522-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2522-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="b2522-106">成員</span><span class="sxs-lookup"><span data-stu-id="b2522-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2522-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="b2522-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="b2522-108">列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2522-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2522-109">**NextJobId**</span><span class="sxs-lookup"><span data-stu-id="b2522-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="b2522-110">在一組連結的列印工作中，下一個列印工作的列印工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2522-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="b2522-111">**已保留**</span><span class="sxs-lookup"><span data-stu-id="b2522-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b2522-112">這個值已保留供未來使用</span><span class="sxs-lookup"><span data-stu-id="b2522-112">This value is reserved for future use.</span></span> <span data-ttu-id="b2522-113">您必須將它設定為零。</span><span class="sxs-lookup"><span data-stu-id="b2522-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2522-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2522-114">Requirements</span></span>



| <span data-ttu-id="b2522-115">需求</span><span class="sxs-lookup"><span data-stu-id="b2522-115">Requirement</span></span> | <span data-ttu-id="b2522-116">值</span><span class="sxs-lookup"><span data-stu-id="b2522-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2522-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2522-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b2522-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2522-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2522-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2522-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b2522-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2522-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2522-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b2522-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2522-122"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b2522-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2522-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2522-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2522-124">列印</span><span class="sxs-lookup"><span data-stu-id="b2522-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b2522-125">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="b2522-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b2522-126">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="b2522-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="b2522-127">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="b2522-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="b2522-128">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="b2522-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




