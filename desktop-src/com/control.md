---
title: 控制
description: 將物件識別為 ActiveX 控制項。
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- 控制登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372631"
---
# <a name="control"></a><span data-ttu-id="7ab1d-104">控制</span><span class="sxs-lookup"><span data-stu-id="7ab1d-104">Control</span></span>

<span data-ttu-id="7ab1d-105">將物件識別為 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="7ab1d-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7ab1d-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="7ab1d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="7ab1d-107">備註</span><span class="sxs-lookup"><span data-stu-id="7ab1d-107">Remarks</span></span>

<span data-ttu-id="7ab1d-108">容器會使用這個選擇性專案來填滿對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7ab1d-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="7ab1d-109">容器會使用這個子機碼來判斷是否要在顯示 ActiveX 控制項的對話方塊中包含物件。</span><span class="sxs-lookup"><span data-stu-id="7ab1d-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="7ab1d-110">如果控制項設計成隻能搭配特定容器運作，因此不適合插入其他容器中，則控制項可以省略此專案。</span><span class="sxs-lookup"><span data-stu-id="7ab1d-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




