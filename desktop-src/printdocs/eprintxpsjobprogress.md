---
description: 指定多工緩衝處理程式處理 XPS 列印工作時的目前執行內容。
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: 'EPrintXPSJobProgress 列舉 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513689"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="484be-103">EPrintXPSJobProgress 列舉</span><span class="sxs-lookup"><span data-stu-id="484be-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="484be-104">指定多工緩衝處理程式處理 XPS 列印工作時的目前執行內容。</span><span class="sxs-lookup"><span data-stu-id="484be-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="484be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="484be-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="484be-106">常數</span><span class="sxs-lookup"><span data-stu-id="484be-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="484be-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="484be-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="484be-108">檔順序即將新增至 XPS 工作。</span><span class="sxs-lookup"><span data-stu-id="484be-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span><span class="sxs-lookup"><span data-stu-id="484be-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="484be-110">已將檔順序新增至 XPS 工作。</span><span class="sxs-lookup"><span data-stu-id="484be-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span><span class="sxs-lookup"><span data-stu-id="484be-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="484be-112">固定檔即將新增至 XPS 工作。</span><span class="sxs-lookup"><span data-stu-id="484be-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span><span class="sxs-lookup"><span data-stu-id="484be-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="484be-114">XPS 工作已新增固定檔。</span><span class="sxs-lookup"><span data-stu-id="484be-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span><span class="sxs-lookup"><span data-stu-id="484be-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="484be-116">頁面即將新增至 XPS 工作。</span><span class="sxs-lookup"><span data-stu-id="484be-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span><span class="sxs-lookup"><span data-stu-id="484be-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="484be-118">XPS 工作已加入頁面。</span><span class="sxs-lookup"><span data-stu-id="484be-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span><span class="sxs-lookup"><span data-stu-id="484be-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="484be-120">已將資源新增至 XPS 工作。</span><span class="sxs-lookup"><span data-stu-id="484be-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span><span class="sxs-lookup"><span data-stu-id="484be-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="484be-122">XPS 工作已新增字型。</span><span class="sxs-lookup"><span data-stu-id="484be-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span><span class="sxs-lookup"><span data-stu-id="484be-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="484be-124">已將映射新增至 XPS 工作。</span><span class="sxs-lookup"><span data-stu-id="484be-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="484be-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span><span class="sxs-lookup"><span data-stu-id="484be-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="484be-126">已認可 XPS 工作的資料。</span><span class="sxs-lookup"><span data-stu-id="484be-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="484be-127">備註</span><span class="sxs-lookup"><span data-stu-id="484be-127">Remarks</span></span>

<span data-ttu-id="484be-128">這個列舉主要是用來做為 [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) 函式的參數。</span><span class="sxs-lookup"><span data-stu-id="484be-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="484be-129">這些值可以指的是列印工作的幕後處理或轉譯階段。</span><span class="sxs-lookup"><span data-stu-id="484be-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="484be-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="484be-130">Requirements</span></span>



| <span data-ttu-id="484be-131">需求</span><span class="sxs-lookup"><span data-stu-id="484be-131">Requirement</span></span> | <span data-ttu-id="484be-132">值</span><span class="sxs-lookup"><span data-stu-id="484be-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="484be-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="484be-133">Minimum supported client</span></span><br/> | <span data-ttu-id="484be-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="484be-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="484be-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="484be-135">Minimum supported server</span></span><br/> | <span data-ttu-id="484be-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="484be-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="484be-137">標頭</span><span class="sxs-lookup"><span data-stu-id="484be-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="484be-138"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="484be-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




