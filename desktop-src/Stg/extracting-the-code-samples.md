---
title: 解壓縮程式代碼範例
description: 雖然程式碼範例分為一系列的教學課程，但是可以輕鬆地從集合中解壓縮適當的範例分組。
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372057"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="11a25-103">解壓縮程式代碼範例</span><span class="sxs-lookup"><span data-stu-id="11a25-103">Extracting the Code Samples</span></span>

<span data-ttu-id="11a25-104">雖然程式碼範例分為一系列的教學課程，但是可以輕鬆地從集合中解壓縮適當的範例分組。</span><span class="sxs-lookup"><span data-stu-id="11a25-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="11a25-105">大部分的個別範例目錄都是要與至少一個其他範例目錄一起使用。</span><span class="sxs-lookup"><span data-stu-id="11a25-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="11a25-106">元件相關的範例是由用戶端和伺服器組所組成，而伺服器則需要使用註冊範例公用程式。</span><span class="sxs-lookup"><span data-stu-id="11a25-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="11a25-107">以下是範例分組的摘要，以及如何將每個群組解壓縮為可建置單位。</span><span class="sxs-lookup"><span data-stu-id="11a25-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="11a25-108">針對每個範例群組，複製所顯示目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="11a25-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="11a25-109">\[所顯示的父目的地 \] 目錄不需要來自範例分支的內容。</span><span class="sxs-lookup"><span data-stu-id="11a25-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="11a25-110">不過，執行中範例中的 [說明] 功能表會假設有適當的教學課程。HTM 說明檔位於這個上層 \[ 目的地 \] 目錄。</span><span class="sxs-lookup"><span data-stu-id="11a25-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="11a25-111">針對 Win32 READTUT 應用程式：</span><span class="sxs-lookup"><span data-stu-id="11a25-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="11a25-112">針對 Win32 EXE 基本架構應用程式：</span><span class="sxs-lookup"><span data-stu-id="11a25-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="11a25-113">針對 Win32 DLL 基本架構：</span><span class="sxs-lookup"><span data-stu-id="11a25-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="11a25-114">針對基本 COM 物件範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="11a25-115">針對基本同進程 DLL 元件用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="11a25-116">如需授權的元件用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="11a25-117">針對標準封送處理範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="11a25-118">針對跨進程本機用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-118">For the out-of-process local client/server samples:</span></span>

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

<span data-ttu-id="11a25-119">針對單元模型用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-119">For the apartment model client/server samples:</span></span>

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

<span data-ttu-id="11a25-120">針對 DCOM (分散式 COM) 用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-120">For the DCOM (Distributed COM) client/server samples:</span></span>

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

<span data-ttu-id="11a25-121">針對免費執行緒用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="11a25-122">針對可連接的 COM 物件用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="11a25-123">針對結構化儲存體用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="11a25-124">針對持續性物件用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-124">For the persistent object client/server samples:</span></span>

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

<span data-ttu-id="11a25-125">針對 DCOM 安全性用戶端/伺服器範例：</span><span class="sxs-lookup"><span data-stu-id="11a25-125">For the DCOM security client/server samples:</span></span>

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

 

 




