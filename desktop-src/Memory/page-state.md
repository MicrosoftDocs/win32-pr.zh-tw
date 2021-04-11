---
description: 進程的虛擬位址空間的頁面可以是下列其中一種狀態。
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: 頁面狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a1e5d3170197cf977f0b1a91898ee150086ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195423"
---
# <a name="page-state"></a>頁面狀態

進程的虛擬位址空間的頁面可以是下列其中一種狀態。



| 州     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 免費      | 此頁面不會認可也不會保留。 此頁面無法供進程存取。 您可以保留、認可或同時保留和認可。 嘗試讀取或寫入免費頁面會導致存取違規例外狀況。 <br/> 處理常式可以使用 [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) 或 [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) 函式來釋出其位址空間的保留或認可頁面，並將它們傳回至可用狀態。<br/>                                                                                                                                                                                                                                                                                                                              |
| 保留  | 頁面已保留供日後使用。 其他配置函數無法使用位址範圍。 頁面無法存取，而且沒有相關聯的實體儲存體。 您可以進行認可。 <br/> 處理常式可以使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 或 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) 函式來保留其位址空間的頁面，並于稍後認可保留的頁面。 它可以使用 [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) 或 [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) 來取消認可認可的頁面，並將其傳回至保留的狀態。<br/>                                                                                                                                                                                                                          |
| 認可 | 記憶體費用是從磁片上的整體 RAM 和分頁檔案的整體大小所配置。 此頁面可供存取，而且存取是由其中一種 [記憶體保護常數](memory-protection-constants.md)所控制。 系統只會在第一次嘗試讀取或寫入至該頁面時，初始化並將每個認可的頁面載入實體記憶體中。 當程式終止時，系統會釋放認可頁面的儲存體。 <br/> 處理常式可以使用 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 或 [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) 來認可保留區域中的實體頁面。 它們也可以同時保留和認可頁面。<br/> [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)和 [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)函式會使用讀取/寫入存取權來配置認可的頁面。<br/> |



 

 

 
