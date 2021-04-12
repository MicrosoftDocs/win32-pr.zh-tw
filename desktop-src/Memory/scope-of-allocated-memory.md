---
description: 進程所配置的所有記憶體都會使用記憶體配置函數 ( HeapAlloc、VirtualAlloc、GlobalAlloc 或 LocalAlloc) 僅供進程存取。
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: 配置的記憶體範圍
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d2db67a04c019683e737d0f9c581ce8d16b800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191504"
---
# <a name="scope-of-allocated-memory"></a>配置的記憶體範圍

進程所配置的所有記憶體都會使用記憶體配置函數 ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)、 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)、 [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)或 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) 僅供進程存取。 不過，DLL 配置的記憶體會配置在呼叫 DLL 之進程的位址空間中，且使用相同 DLL 無法存取其他進程。 若要建立共用記憶體，您必須使用檔案對應。

命名檔案對應提供簡單的方法來建立共用記憶體區塊。 當進程使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 函式來建立檔案對應物件時，可以指定名稱。 其他進程可以為 **CreateFileMapping** 或 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式指定相同的名稱，以取得對應物件的控制碼。

每個進程會在 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 函式中指定其檔案對應物件的控制碼，以將檔案的視圖對應到它自己的位址空間。 單一檔案對應物件的所有進程的視圖都會對應到相同的可共用的實體儲存體頁面。 不過，除非使用 [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) 函式將視圖對應到指定的位址，否則對應視圖的虛擬位址可能會從一個進程變更為另一個進程。 雖然可共用，但用於對應檔案視圖的實體儲存體頁面並不是全域的，尚未對應檔案視圖的進程無法存取它們。

藉由對應檔案的視圖所認可的任何頁面，會在最後一個處理常式的對應物件結束時釋出，或是藉由呼叫 [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) 函數來 unmaps 其觀點。 目前，指定的檔案 (是否已更新與對應物件相關聯的任何) 。 您也可以藉由呼叫 [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) 函數，強制更新指定的檔案。

如需詳細資訊，請參閱檔案 [對應](file-mapping.md)。 如需 DLL 中共用記憶體的範例，請參閱 [使用 Dynamic-Link 程式庫中的共用記憶體](../dlls/using-shared-memory-in-a-dynamic-link-library.md)。

如果多個進程具有共用記憶體的寫入存取權，您就必須同步處理記憶體的存取。 如需詳細資訊，請參閱 [同步](../sync/synchronization.md)處理。

 

 
