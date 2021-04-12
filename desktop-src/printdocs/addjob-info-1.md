---
description: SYSTEM.PRINTING.PRINTQUEUE.ADDJOB \_ INFO \_ 1 結構會識別列印工作，以及應用程式可以儲存該作業的目錄和檔案。
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: 'ADDJOB_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194972"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="b1eed-103">SYSTEM.PRINTING.PRINTQUEUE.ADDJOB \_ INFO \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="b1eed-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="b1eed-104">**System.printing.printqueue.addjob \_ INFO \_ 1** 結構會識別列印工作，以及應用程式可以儲存該作業的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="b1eed-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1eed-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1eed-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="b1eed-106">成員</span><span class="sxs-lookup"><span data-stu-id="b1eed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1eed-107">**路徑**</span><span class="sxs-lookup"><span data-stu-id="b1eed-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="b1eed-108">以 null 結束的字串指標，其中包含應用程式可以用來儲存列印工作的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="b1eed-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="b1eed-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="b1eed-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="b1eed-110">列印工作的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b1eed-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1eed-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1eed-111">Requirements</span></span>



| <span data-ttu-id="b1eed-112">需求</span><span class="sxs-lookup"><span data-stu-id="b1eed-112">Requirement</span></span> | <span data-ttu-id="b1eed-113">值</span><span class="sxs-lookup"><span data-stu-id="b1eed-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1eed-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1eed-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b1eed-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1eed-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b1eed-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1eed-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b1eed-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1eed-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1eed-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b1eed-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1eed-119"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b1eed-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b1eed-120">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b1eed-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b1eed-121">**\_ System.printing.printqueue.addjob \_ Info \_ 1W** (Unicode) 和 **\_ system.printing.printqueue.addjob \_ info \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b1eed-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="b1eed-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1eed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1eed-123">列印</span><span class="sxs-lookup"><span data-stu-id="b1eed-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b1eed-124">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="b1eed-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b1eed-125">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="b1eed-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




