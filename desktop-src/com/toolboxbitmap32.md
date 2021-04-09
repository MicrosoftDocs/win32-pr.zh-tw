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
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

識別要用於工具列或工具箱按鈕臉部的 16 x 16 點陣圖的模組名稱和資源識別碼。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定點陣圖的模組名稱和資源識別碼。

標準 Windows 圖示大小太大，無法用於此用途。 這需要具有設計模式的控制項容器，其中一個會選取控制項，並將其放在所設計的表單上。

 

 




