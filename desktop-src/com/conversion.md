---
title: 轉換
description: 由 [轉換] 對話方塊用來判斷應用程式可以讀取和寫入的格式。
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- 轉換登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507437"
---
# <a name="conversion"></a><span data-ttu-id="81915-104">轉換</span><span class="sxs-lookup"><span data-stu-id="81915-104">Conversion</span></span>

<span data-ttu-id="81915-105">由 [ **轉換** ] 對話方塊用來判斷應用程式可以讀取和寫入的格式。</span><span class="sxs-lookup"><span data-stu-id="81915-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="81915-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="81915-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="81915-107">備註</span><span class="sxs-lookup"><span data-stu-id="81915-107">Remarks</span></span>

<span data-ttu-id="81915-108">**轉換對話方塊會** 使用轉換資訊來判斷應用程式可以讀取和寫入的格式。</span><span class="sxs-lookup"><span data-stu-id="81915-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="81915-109">以逗號分隔的檔案格式是以數位表示（如果它是 Windows 中所定義的其中一個剪貼簿格式）。</span><span class="sxs-lookup"><span data-stu-id="81915-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="81915-110">字串表示格式不是在 Windows .h (私用) 中定義。</span><span class="sxs-lookup"><span data-stu-id="81915-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="81915-111">在此情況下，可讀取和可寫入的格式為 \_ (私用) 的 CF 大綱。</span><span class="sxs-lookup"><span data-stu-id="81915-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="81915-112">*Rformat* 值會指定應用程式可以讀取的檔案格式 (從) 轉換。</span><span class="sxs-lookup"><span data-stu-id="81915-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="81915-113">*Rwformat* 值會指定應用程式可以讀取和寫入的檔案格式 (啟動為) 。</span><span class="sxs-lookup"><span data-stu-id="81915-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




