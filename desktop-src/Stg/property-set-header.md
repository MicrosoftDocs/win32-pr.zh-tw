---
title: 屬性集標頭
description: 屬性集資料流程的開頭是標頭。 它是由位元組順序指標、格式版本、原始作業系統版本、類別識別碼 (CLSID) 和保留字段所組成。
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- 屬性集標頭結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662218"
---
# <a name="property-set-header"></a>屬性集標頭

屬性集資料流程的開頭是標頭。 它是由位元組順序指標、格式版本、原始作業系統版本、類別識別碼 (CLSID) 和保留字段所組成。

下列虛擬結構說明標頭。

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




