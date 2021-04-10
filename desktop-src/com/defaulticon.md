---
title: DefaultIcon
description: 提供 iconic 物件簡報的預設圖示資訊。
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024147"
---
# <a name="defaulticon"></a><span data-ttu-id="05c20-104">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="05c20-104">DefaultIcon</span></span>

<span data-ttu-id="05c20-105">提供 iconic 物件簡報的預設圖示資訊。</span><span class="sxs-lookup"><span data-stu-id="05c20-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="05c20-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="05c20-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="05c20-107">備註</span><span class="sxs-lookup"><span data-stu-id="05c20-107">Remarks</span></span>

<span data-ttu-id="05c20-108">這是 **REG \_ SZ** 值，可指定物件應用程式之可執行檔名稱的完整路徑，以及可執行檔中圖示的資源索引。</span><span class="sxs-lookup"><span data-stu-id="05c20-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="05c20-109">例如，當控制項最小化至圖示時， **DefaultIcon** 會識別要使用的圖示。</span><span class="sxs-lookup"><span data-stu-id="05c20-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="05c20-110">此專案包含伺服器應用程式之可執行檔名稱的完整路徑，以及可執行檔中圖示的資源索引。</span><span class="sxs-lookup"><span data-stu-id="05c20-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="05c20-111">應用程式可以使用 **DefaultIcon** 所提供的資訊，透過 [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona)取得圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="05c20-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 