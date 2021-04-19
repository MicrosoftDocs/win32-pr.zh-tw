---
description: DOC \_ 資訊 \_ 3 結構描述將列印的檔。
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: 'DOC_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987515"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="e6b9e-103">DOC \_ 資訊 \_ 3 結構</span><span class="sxs-lookup"><span data-stu-id="e6b9e-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="e6b9e-104">**DOC \_ 資訊 \_ 3** 結構描述將列印的檔。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6b9e-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="e6b9e-106">成員</span><span class="sxs-lookup"><span data-stu-id="e6b9e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6b9e-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="e6b9e-108">指定檔案名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="e6b9e-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="e6b9e-110">指定輸出檔名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="e6b9e-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="e6b9e-112">以 null 結束的字串指標，識別用來記錄檔的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="e6b9e-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e6b9e-114">標誌。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-114">Flags.</span></span> <span data-ttu-id="e6b9e-115">目前，它可以是 **Null** 或下列值。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="e6b9e-116">旗標</span><span class="sxs-lookup"><span data-stu-id="e6b9e-116">Flag</span></span>                 | <span data-ttu-id="e6b9e-117">意義</span><span class="sxs-lookup"><span data-stu-id="e6b9e-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b9e-118">DI \_ MEMORYMAP \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="e6b9e-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="e6b9e-119">讓 [**StartDocPrinter**](startdocprinter.md) 不會使用 [**system.printing.printqueue.addjob**](addjob.md) 和 [**ScheduleJob**](schedulejob.md) 進行本機列印。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6b9e-120">備註</span><span class="sxs-lookup"><span data-stu-id="e6b9e-120">Remarks</span></span>

<span data-ttu-id="e6b9e-121">\_ \_ **DOC \_ 資訊 \_ 3** 中的 DI MEMORYMAP 寫入設定是一項優化。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="e6b9e-122">這可讓 GDI 在應用程式中對應多工緩衝處理檔案，並加速錄製。</span><span class="sxs-lookup"><span data-stu-id="e6b9e-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b9e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6b9e-123">Requirements</span></span>



| <span data-ttu-id="e6b9e-124">需求</span><span class="sxs-lookup"><span data-stu-id="e6b9e-124">Requirement</span></span> | <span data-ttu-id="e6b9e-125">值</span><span class="sxs-lookup"><span data-stu-id="e6b9e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b9e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6b9e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b9e-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6b9e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e6b9e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6b9e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b9e-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6b9e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e6b9e-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e6b9e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6b9e-131"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e6b9e-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e6b9e-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e6b9e-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e6b9e-133">**\_ Doc \_ 資訊 \_ 3w 法** (Unicode) 和 **\_ doc \_ 資訊 \_ 3a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e6b9e-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="e6b9e-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6b9e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6b9e-135">列印</span><span class="sxs-lookup"><span data-stu-id="e6b9e-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e6b9e-136">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="e6b9e-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e6b9e-137">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="e6b9e-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="e6b9e-139">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="e6b9e-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




