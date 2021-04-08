---
title: AutoConvertTo
description: 指定將物件的指定類別自動轉換成物件的新類別。
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- AutoConvertTo 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839068"
---
# <a name="autoconvertto"></a><span data-ttu-id="46693-104">AutoConvertTo</span><span class="sxs-lookup"><span data-stu-id="46693-104">AutoConvertTo</span></span>

<span data-ttu-id="46693-105">指定將物件的指定類別自動轉換成物件的新類別。</span><span class="sxs-lookup"><span data-stu-id="46693-105">Specifies the automatic conversion of a given class of objects to a new class of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="46693-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="46693-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a><span data-ttu-id="46693-107">備註</span><span class="sxs-lookup"><span data-stu-id="46693-107">Remarks</span></span>

<span data-ttu-id="46693-108">這是 **REG \_ SZ** 值，可指定物件的類別識別碼，該物件為物件的指定物件或類別應轉換成的物件。</span><span class="sxs-lookup"><span data-stu-id="46693-108">This is a **REG\_SZ** value that specifies the class identifier of the object to which the given object or class of objects should be converted.</span></span>

<span data-ttu-id="46693-109">此索引鍵通常用來將繼承應用程式所建立的檔案，自動轉換為較新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="46693-109">This key is typically used to automatically convert files created by an older version of an application to a newer version of the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46693-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="46693-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46693-111">**OleDoAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="46693-111">**OleDoAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[<span data-ttu-id="46693-112">**OleGetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="46693-112">**OleGetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[<span data-ttu-id="46693-113">**OleSetAutoConvert**</span><span class="sxs-lookup"><span data-stu-id="46693-113">**OleSetAutoConvert**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




