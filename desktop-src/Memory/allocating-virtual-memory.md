---
description: 虛擬記憶體函式會操作分頁的記憶體。 這些函數會使用目前電腦上的頁面大小，來將指定的大小和位址四捨五入。
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: 配置虛擬記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77039db22d4a9d2897e1269e3ee82902c81fae2274bea12d5a7f7abbaa9e7d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963468"
---
# <a name="allocating-virtual-memory"></a>配置虛擬記憶體

虛擬記憶體函式會操作分頁的記憶體。 這些函數會使用目前電腦上的頁面大小，來將指定的大小和位址四捨五入。

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)函式會執行下列其中一項作業：

-   保留一或多個可用的頁面。
-   認可一或多個保留的頁面。
-   保留並認可一或多個可用的頁面。

您可以指定要保留或認可之頁面的起始位址，也可以讓系統判斷位址。 函數會將指定的位址四捨五入至適當的頁面界限。 保留的頁面無法存取，但是認可的頁面可以使用 **page \_ READWRITE**、 **page \_ READONLY** 或 **page \_ NOACCESS** access 來配置。 認可頁面時，會從 RAM 的整體大小和磁片上的分頁檔案配置記憶體費用，但每個頁面只會在第一次嘗試讀取或寫入該頁面時，初始化並載入實體記憶體中。 您可以使用一般指標參考來存取 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 函數所認可的記憶體。

 

 
