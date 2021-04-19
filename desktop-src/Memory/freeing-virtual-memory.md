---
description: VirtualFree 函式會根據下列規則來解除和釋放頁面。
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: 釋放虛擬記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973827"
---
# <a name="freeing-virtual-memory"></a>釋放虛擬記憶體

[**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)函式會根據下列規則來解除和釋放頁面：

-   解除一或多個認可的頁面，並將頁面的狀態變更為「已保留」。 Decommitting 頁面會釋放與頁面相關聯的實體儲存體，使其可供任何程式配置。 您可以已取消認可任何已認可頁面的區塊。
-   釋放一或多個保留頁面的區塊，將頁面的狀態變更為「可用」。 釋出頁面區塊，可讓處理常式配置保留位址的範圍。 只有釋放 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)最初保留的整個區塊，才能釋放保留的頁面。
-   將一或多個認可頁面的區塊同時解除鎖定，並將頁面的狀態變更為「可用」。 指定的區塊必須包含最初由 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)保留的整個區塊，而且所有的頁面都必須目前已認可。

當記憶體區塊釋出或已取消認可之後，您就不能再次參考它。 在該記憶體中可能存在的任何資訊都將永遠消失。 嘗試讀取或寫入免費頁面會導致存取違規例外狀況。 如果您需要資訊，請勿取消認可或釋放包含該資訊的記憶體。

若要指定不再有興趣的記憶體範圍中的資料，請使用 VirtualAlloc **\_ 重設** 來呼叫 [](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 。 頁面不會讀取或寫入分頁檔案。 不過，您可以稍後再使用記憶體區塊。

 

 
