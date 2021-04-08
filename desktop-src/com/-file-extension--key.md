---
title: file_extension 金鑰
description: 將副檔名與 ProgID 產生關聯。
ms.assetid: 018998a8-c0da-43ea-bae2-3b184897eb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e602266f3c851975c2f8e008ced5dfc8e2d40b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840795"
---
# <a name="file_extension-key"></a><span data-ttu-id="1818a-103"><\_ 副檔名> 金鑰</span><span class="sxs-lookup"><span data-stu-id="1818a-103"><file\_extension> Key</span></span>

<span data-ttu-id="1818a-104">將副檔名與 ProgID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1818a-104">Associates a file name extension with a ProgID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1818a-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="1818a-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   .ext = ProgID
```

## <a name="remarks"></a><span data-ttu-id="1818a-106">備註</span><span class="sxs-lookup"><span data-stu-id="1818a-106">Remarks</span></span>

<span data-ttu-id="1818a-107">副檔名中包含的資訊是由 Windows 檔案總管和檔案的名字標記所使用。</span><span class="sxs-lookup"><span data-stu-id="1818a-107">The information contained in the file name extension key is used by both the Windows Explorer and file monikers.</span></span> <span data-ttu-id="1818a-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) 使用副檔名來提供相關聯的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="1818a-108">[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) uses the file name extension key to supply the associated CLSID.</span></span>

<span data-ttu-id="1818a-109">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。</span><span class="sxs-lookup"><span data-stu-id="1818a-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1818a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="1818a-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1818a-111">**FileType**</span><span class="sxs-lookup"><span data-stu-id="1818a-111">**FileType**</span></span>](filetype-key.md)
</dt> <dt>

[<span data-ttu-id="1818a-112">**GetClassFile**</span><span class="sxs-lookup"><span data-stu-id="1818a-112">**GetClassFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




