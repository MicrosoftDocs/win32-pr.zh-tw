---
title: 屬性集標頭
description: 屬性集資料流程的開頭是標頭。 它是由位元組順序指標、格式版本、原始作業系統版本、類別識別碼 (CLSID) 和保留字段所組成。
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- 屬性集標頭結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311576"
---
# <a name="property-set-header"></a><span data-ttu-id="69330-105">屬性集標頭</span><span class="sxs-lookup"><span data-stu-id="69330-105">Property Set Header</span></span>

<span data-ttu-id="69330-106">屬性集資料流程的開頭是標頭。</span><span class="sxs-lookup"><span data-stu-id="69330-106">At the beginning of the property set stream is a header.</span></span> <span data-ttu-id="69330-107">它是由位元組順序指標、格式版本、原始作業系統版本、類別識別碼 (CLSID) 和保留字段所組成。</span><span class="sxs-lookup"><span data-stu-id="69330-107">It consists of a byte-order indicator, a format version, the originating operating system version, the class identifier (CLSID), and a reserved field.</span></span>

<span data-ttu-id="69330-108">下列虛擬結構說明標頭。</span><span class="sxs-lookup"><span data-stu-id="69330-108">The following pseudo-structure illustrates the header.</span></span>

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

 

 




