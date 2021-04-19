---
description: DOC \_ INFO \_ 2 結構描述將列印的檔。
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: 'DOC_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987729"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="10c9d-103">DOC \_ INFO \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="10c9d-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="10c9d-104">**DOC \_ INFO \_ 2** 結構描述將列印的檔。</span><span class="sxs-lookup"><span data-stu-id="10c9d-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c9d-105">語法</span><span class="sxs-lookup"><span data-stu-id="10c9d-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="10c9d-106">成員</span><span class="sxs-lookup"><span data-stu-id="10c9d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="10c9d-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="10c9d-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="10c9d-108">指定檔案名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="10c9d-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="10c9d-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="10c9d-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="10c9d-110">指定輸出檔名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="10c9d-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="10c9d-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="10c9d-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="10c9d-112">以 null 結束的字串指標，識別用來記錄檔的資料類型。</span><span class="sxs-lookup"><span data-stu-id="10c9d-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="10c9d-113">**dwMode**</span><span class="sxs-lookup"><span data-stu-id="10c9d-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="10c9d-114">通知「列印多工緩衝處理器」所要遵循的資料本質。</span><span class="sxs-lookup"><span data-stu-id="10c9d-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="10c9d-115">如果這個值為零，列印多工緩衝處理器會將後續呼叫 [**WritePrinter**](writeprinter.md) 所傳送的資料視為一般列印工作， (是否要將它進行多工緩衝處理，取決於印表機屬性) 。</span><span class="sxs-lookup"><span data-stu-id="10c9d-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="10c9d-116">如果此值為 DI \_ 通道，則只會開啟通道。</span><span class="sxs-lookup"><span data-stu-id="10c9d-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="10c9d-117">在此情況下，傳遞至 **WritePrinter** 後續呼叫的資料會傳送至印表機，或後續對 [**ReadPrinter**](readprinter.md) 的呼叫會從印表機取出資料。</span><span class="sxs-lookup"><span data-stu-id="10c9d-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="10c9d-118">這個模式會維持有效，直到呼叫 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 為止。</span><span class="sxs-lookup"><span data-stu-id="10c9d-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="10c9d-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="10c9d-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="10c9d-120">保留供內部使用;應為零。</span><span class="sxs-lookup"><span data-stu-id="10c9d-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10c9d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="10c9d-121">Requirements</span></span>



| <span data-ttu-id="10c9d-122">需求</span><span class="sxs-lookup"><span data-stu-id="10c9d-122">Requirement</span></span> | <span data-ttu-id="10c9d-123">值</span><span class="sxs-lookup"><span data-stu-id="10c9d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10c9d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10c9d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="10c9d-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10c9d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10c9d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10c9d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="10c9d-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10c9d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="10c9d-128">標頭</span><span class="sxs-lookup"><span data-stu-id="10c9d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="10c9d-129"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="10c9d-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="10c9d-130">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="10c9d-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="10c9d-131">**\_ Doc \_ 資訊 \_ 2w** (Unicode) 和 **\_ DOC \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="10c9d-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="10c9d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10c9d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c9d-133">列印</span><span class="sxs-lookup"><span data-stu-id="10c9d-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="10c9d-134">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="10c9d-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="10c9d-135">**EndDoc**</span><span class="sxs-lookup"><span data-stu-id="10c9d-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="10c9d-136">**ReadPrinter**</span><span class="sxs-lookup"><span data-stu-id="10c9d-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="10c9d-137">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="10c9d-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="10c9d-138">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="10c9d-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




