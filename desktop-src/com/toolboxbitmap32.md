---
title: ToolBoxBitmap32
description: 識別要用於工具列或工具箱按鈕臉部的 16 x 16 點陣圖的模組名稱和資源識別碼。
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- ToolBoxBitmap32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021270"
---
# <a name="toolboxbitmap32"></a><span data-ttu-id="e38bb-104">ToolBoxBitmap32</span><span class="sxs-lookup"><span data-stu-id="e38bb-104">ToolBoxBitmap32</span></span>

<span data-ttu-id="e38bb-105">識別要用於工具列或工具箱按鈕臉部的 16 x 16 點陣圖的模組名稱和資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e38bb-105">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e38bb-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="e38bb-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a><span data-ttu-id="e38bb-107">備註</span><span class="sxs-lookup"><span data-stu-id="e38bb-107">Remarks</span></span>

<span data-ttu-id="e38bb-108">這是 **REG \_ SZ** 值，可指定點陣圖的模組名稱和資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e38bb-108">This is a **REG\_SZ** value that specifies the module name and resource identifier for the bitmap.</span></span>

<span data-ttu-id="e38bb-109">標準 Windows 圖示大小太大，無法用於此用途。</span><span class="sxs-lookup"><span data-stu-id="e38bb-109">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="e38bb-110">這需要具有設計模式的控制項容器，其中一個會選取控制項，並將其放在所設計的表單上。</span><span class="sxs-lookup"><span data-stu-id="e38bb-110">This requires control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span>

 

 




