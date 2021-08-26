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
ms.openlocfilehash: ef3d72d983388c022afbb0e914f87a17587f70b8e175dd57dabcd61d224e93bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949638"
---
# <a name="eprintxpsjobprogress-enumeration"></a>EPrintXPSJobProgress 列舉

指定多工緩衝處理程式處理 XPS 列印工作時的目前執行內容。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**
</dt> <dd>

檔順序即將新增至 XPS 工作。

</dd> <dt>

<span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**
</dt> <dd>

已將檔順序新增至 XPS 工作。

</dd> <dt>

<span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**
</dt> <dd>

固定檔即將新增至 XPS 工作。

</dd> <dt>

<span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**
</dt> <dd>

XPS 工作已新增固定檔。

</dd> <dt>

<span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**
</dt> <dd>

頁面即將新增至 XPS 工作。

</dd> <dt>

<span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**
</dt> <dd>

XPS 工作已加入頁面。

</dd> <dt>

<span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**
</dt> <dd>

已將資源新增至 XPS 工作。

</dd> <dt>

<span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**
</dt> <dd>

XPS 工作已新增字型。

</dd> <dt>

<span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**
</dt> <dd>

已將映射新增至 XPS 工作。

</dd> <dt>

<span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**
</dt> <dd>

已認可 XPS 工作的資料。

</dd> </dl>

## <a name="remarks"></a>備註

這個列舉主要是用來做為 [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) 函式的參數。

這些值可以指的是列印工作的幕後處理或轉譯階段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



 

 




