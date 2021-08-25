---
title: 解壓縮程式代碼範例
description: 雖然程式碼範例分為一系列的教學課程，但是可以輕鬆地從集合中解壓縮適當的範例分組。
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67093f4cfbbfab2a3c1681462627f02b504124ed15d1483b9f9d91ec5551d0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034948"
---
# <a name="extracting-the-code-samples"></a>解壓縮程式代碼範例

雖然程式碼範例分為一系列的教學課程，但是可以輕鬆地從集合中解壓縮適當的範例分組。 大部分的個別範例目錄都是要與至少一個其他範例目錄一起使用。 元件相關的範例是由用戶端和伺服器組所組成，而伺服器則需要使用註冊範例公用程式。 以下是範例分組的摘要，以及如何將每個群組解壓縮為可建置單位。 針對每個範例群組，複製所顯示目錄的內容。 \[所顯示的父目的地 \] 目錄不需要來自範例分支的內容。 不過，執行中範例中的 [說明] 功能表會假設適當的教學課程 .HTM 說明檔位於這個父 \[ 目的地 \] 目錄。

針對 Win32 READTUT 應用程式：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

針對 Win32 EXE 基本架構應用程式：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

針對 Win32 DLL 基本架構：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

針對基本 COM 物件範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

針對基本同進程 DLL 元件用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

如需授權的元件用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

針對標準封送處理範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

針對跨進程本機用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

針對單元模型用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

針對 DCOM (分散式 COM) 用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

針對免費執行緒用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

針對可連接的 COM 物件用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

針對結構化儲存體用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

針對持續性物件用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

針對 DCOM 安全性用戶端/伺服器範例：

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




