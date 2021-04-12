---
description: DOC \_ INFO \_ 1 結構描述將列印的檔。
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: 'DOC_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192604"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="c4a73-103">DOC \_ INFO \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="c4a73-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="c4a73-104">**DOC \_ INFO \_ 1** 結構描述將列印的檔。</span><span class="sxs-lookup"><span data-stu-id="c4a73-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a73-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4a73-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="c4a73-106">成員</span><span class="sxs-lookup"><span data-stu-id="c4a73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4a73-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="c4a73-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="c4a73-108">指定檔案名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="c4a73-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="c4a73-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="c4a73-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="c4a73-110">指定輸出檔名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="c4a73-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="c4a73-111">若要列印至印表機，請將此 **值** 設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="c4a73-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4a73-112">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="c4a73-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="c4a73-113">以 null 結束的字串指標，識別用來記錄檔的資料類型。</span><span class="sxs-lookup"><span data-stu-id="c4a73-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4a73-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4a73-114">Requirements</span></span>



| <span data-ttu-id="c4a73-115">需求</span><span class="sxs-lookup"><span data-stu-id="c4a73-115">Requirement</span></span> | <span data-ttu-id="c4a73-116">值</span><span class="sxs-lookup"><span data-stu-id="c4a73-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a73-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4a73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a73-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4a73-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4a73-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4a73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a73-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4a73-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4a73-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c4a73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a73-122"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c4a73-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c4a73-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c4a73-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4a73-124">**\_ Doc \_ 資訊 \_ 1W** (Unicode) 和 **\_ doc \_ info \_ 1a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c4a73-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="c4a73-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4a73-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a73-126">列印</span><span class="sxs-lookup"><span data-stu-id="c4a73-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c4a73-127">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="c4a73-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c4a73-128">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="c4a73-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




