---
description: 本主題說明記憶體管理功能：
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: 記憶體管理函式
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: 635fa59b6a5b6a549438d8bfed71781d6d9e6fa6a9d2c12524684ded28a0f3df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822188"
---
# <a name="memory-management-functions"></a>記憶體管理函式

- [一般記憶體函數](#general-memory-functions)
- [資料執行防止函數](#data-execution-prevention-functions)
- [檔案對應函式](#file-mapping-functions)
- [AWE 函數](#awe-functions)
- [堆積函式](#heap-functions)
- [虛擬記憶體函數](#virtual-memory-functions)
- [全域和區域函數](#global-and-local-functions)
- [錯誤的記憶體函數](#bad-memory-functions)
- [記憶體保護區函式](#enclave-functions)
- [ATL Thunk 函數](#atl-thunk-functions)
- [已淘汰函式](#obsolete-functions)

## <a name="general-memory-functions"></a>一般記憶體函數

| 函式 | 描述 |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | 註冊回呼函式，以在釋放安全的記憶體範圍或其保護變更時呼叫。 |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | 將記憶體區塊從一個位置複製到另一個位置。 |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | 建立記憶體資源通知物件。 |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | 以指定的值填滿記憶體區塊。 |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | 抓取大型頁面的大小下限。 |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | 抓取電腦上實際安裝的 RAM 數量。 |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | 抓取系統快取之工作集目前的大小限制。 |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | 抓取已寫入虛擬記憶體區域中的頁面位址。 |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | 取得系統目前的實體和虛擬記憶體使用量的相關資訊。 |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | 將記憶體區塊從某個位置移到另一個位置。 |
| [**>querymemoryresourcenotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | 抓取指定記憶體資源物件的狀態。 |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | 取消註冊先前向 [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) 函式註冊的回呼函式。 |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | 重設虛擬記憶體區域的寫入追蹤狀態。 |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | 應用程式定義的函式，會在釋放安全的記憶體範圍或其保護變更時呼叫。 |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | 以零填滿記憶體區塊。 |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | 限制檔案系統快取的工作集大小。 |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | 以零填滿記憶體區塊。 |

## <a name="data-execution-prevention-functions"></a>資料執行防止函數

這些函式會與 [資料執行防止](data-execution-prevention.md) (DEP) 搭配使用。

| 函式 | 描述 |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | 抓取進程的 DEP 設定。 |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | 捕獲系統的 DEP 設定。 |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | 變更進程的 DEP 設定。 |

## <a name="file-mapping-functions"></a>檔案對應函式

這些函式會在檔案 [對應](file-mapping.md)中使用。

| 函式 | 描述 |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | 針對指定的檔案，建立或開啟已命名或未命名的檔案對應物件。 |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | 針對指定的檔案，建立或開啟已命名或未命名的檔案對應物件。 |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | 針對指定的檔案，建立或開啟已命名或未命名的檔案對應物件。 您可以指定將實體記憶體的慣用 NUMA 節點指定為擴充參數;請參閱 *ExtendedParameters* 參數。 |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | 針對 Windows 存放區應用程式中指定的檔案，建立或開啟已命名或未命名的檔案對應物件。 |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | 針對指定的檔案建立或開啟已命名或未命名的檔案對應物件，並為實體記憶體指定 NUMA 節點。 |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | 將檔案的對應視圖內的位元組範圍寫入磁片。 |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | 檢查指定的位址是否在指定進程的位址空間中的記憶體對應檔案內。 如果是的話，函數會傳回記憶體對應檔的名稱。 |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | 地圖將檔案對應到呼叫進程的位址空間中的觀點。 |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | 地圖將檔案或分頁檔案的區段視圖至指定進程的位址空間。 |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | 地圖將檔案或分頁檔案的區段視圖至指定進程的位址空間。 |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | 地圖從 Windows Store 應用程式中，將檔案對應到呼叫進程的位址空間的觀點。 |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | 地圖將檔案對應到呼叫進程的位址空間中的觀點。 呼叫者可以選擇性地為視圖指定建議的記憶體位址。 |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | 地圖將檔案對應到呼叫進程的位址空間，並為實體記憶體指定 NUMA 節點。 |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | 地圖從 Windows Store 應用程式中，將檔案對應到呼叫進程的位址空間的觀點。 |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | 地圖將檔案或分頁檔案的區段視圖至指定進程的位址空間。 |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | 開啟命名的檔案對應物件。 |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | 開啟命名的檔案對應物件。 |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | 從呼叫進程的位址空間，Unmaps 檔案的對應視圖。 |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Unmaps 檔案的先前對應視圖或分頁檔的區段。 |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Unmaps 檔案的先前對應視圖或分頁檔的區段。 |

## <a name="awe-functions"></a>AWE 函數

這些是 [AWE 函數](address-windowing-extensions.md)。

| 函式 | 描述 |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | 配置要在進程的任何 AWE 區域內對應和取消對應的實體記憶體頁面。 |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | 配置要在進程的任何 AWE 區域內對應和取消對應的實體記憶體頁面，並為實體記憶體指定 NUMA 節點。 |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | 釋出先前以 [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)配置的實體記憶體頁面。 |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | 地圖先前在 AWE 區域內的指定位址配置的實體記憶體頁面。 |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | 地圖先前在 AWE 區域內的指定位址配置的實體記憶體頁面。 |

## <a name="heap-functions"></a>堆積函式

這些是 [堆積函數](heap-functions.md)。

| 函式 | 描述 |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | 取得呼叫進程堆積的控制碼。 |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | 取得所有對呼叫進程有效之堆積的控制碼。 |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | 從堆積配置記憶體區塊。 |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | 將連續的可用記憶體區塊，在堆積上。 |
| [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | 建立堆積物件。 |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | 終結指定的堆積物件。 |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | 釋放從堆積配置的記憶體區塊。 |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | 嘗試取得與指定堆積相關聯的鎖定。 |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | 抓取指定之堆積的相關資訊。 |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | 從堆積重新配置記憶體區塊。 |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | 設定指定之堆積的堆積資訊。 |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | 捕獲從堆積配置的記憶體區塊大小。 |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | 釋放與指定堆積相關聯之鎖定的擁有權。 |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | 嘗試驗證指定的堆積。 |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | 列舉指定堆積中的記憶體區塊。 |

## <a name="virtual-memory-functions"></a>虛擬記憶體函數

這些是 [虛擬記憶體函數](virtual-memory-functions.md)。

| 函式 | 描述 |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | 捨棄記憶體頁面範圍的記憶體內容，而不 decommitting 記憶體。 捨棄的記憶體內容是未定義的，而且必須由應用程式重寫。 |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | 表示應用程式已不再需要記憶體頁面範圍內所含的資料，而且可以在必要時將它捨棄。 |
| [**PrefetchVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | 將虛擬位址範圍預先提取到實體記憶體中。 |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | 傳回指定進程的虛擬位址空間內，頁面或一組頁面的相關資訊。 |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | 回收以 [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory)提供給系統的記憶體頁面範圍。 |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | 提供 CFG 與有效的間接呼叫目標清單，並指定是否應將它們標記為有效。 |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | 保留或認可呼叫進程之虛擬位址空間中的頁面區域。 |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | 在指定進程的虛擬位址空間內保留、認可或變更記憶體區域的狀態。 函式會將它所配置的記憶體初始化為零。 |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | 在呼叫進程的虛擬位址空間中保留、認可或變更頁面區域的狀態。 此函數所配置的記憶體會自動初始化為零。 |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | 保留或認可指定進程的虛擬位址空間中的頁面區域。 |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | 保留或認可指定進程的虛擬位址空間內的記憶體區域，並指定實體記憶體的 NUMA 節點。 |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | 在呼叫進程的虛擬位址空間中保留、認可或變更頁面區域的狀態。 此函數所配置的記憶體會自動初始化為零。 |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | 在呼叫進程的虛擬位址空間內釋放或解除頁面區域。 |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | 釋放或解除指定進程的虛擬位址空間內的記憶體區域。 |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | 將進程的虛擬位址空間的指定區域鎖定為實體記憶體。 |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | 在呼叫進程的虛擬位址空間中，變更已認可頁面區域的存取保護。 |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | 在呼叫進程的虛擬位址空間中，變更已認可頁面區域的存取保護。 |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | 在呼叫進程的虛擬位址空間中，變更認可頁面區域的保護。 |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | 提供有關呼叫進程的虛擬位址空間中的頁面範圍的資訊。 |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | 提供有關呼叫進程的虛擬位址空間中的頁面範圍的資訊。 |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | 解除鎖定進程的虛擬位址空間中指定的頁面範圍。 |

## <a name="global-and-local-functions"></a>全域和區域函數

另請參閱 [全域和區域函數](global-and-local-functions.md)。 提供這些函式的目的是為了與16位 Windows 的相容性，並搭配動態資料交換 (DDE) 、剪貼簿函式和 OLE 資料物件使用。 除非檔特別指出應該使用全域或區域函式，否則新的應用程式應該使用對應的 [堆積函數](heap-functions.md) 搭配 [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap)所傳回的控制碼。 針對全域或區域函式的對等功能，將堆積函數的 *dwFlags* 參數設定為0。

| 函式 | 描述 | 對應的堆積函數 |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)、 [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | 從堆積配置指定的位元組數目。 | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard)、 [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | 捨棄指定的全域記憶體區塊。 | 不適用。 |
| [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags)、 [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | 傳回指定之全域記憶體物件的相關資訊。 | 不適用。 使用 [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) 來驗證堆積。 |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)、 [ **>localfree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | 釋出指定的全域記憶體物件。 | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle)、 [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | 抓取與全域記憶體區塊之指定指標相關聯的控制碼。 此函數只能搭配需要的 OLE 和剪貼簿函式使用。 | 不適用。 |
| [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock)、 [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | 鎖定全域記憶體物件，並將指標傳回物件之記憶體區塊的第一個位元組。 | 不適用。 |
| [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)、 [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | 變更指定之全域記憶體物件的大小或屬性。 | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize)、 [ **LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | 抓取指定之全域記憶體物件的目前大小。 | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**GlobalUnlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock)、 [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | 遞減與記憶體物件相關聯的鎖定計數。 此函數只能搭配需要的 OLE 和剪貼簿函式使用。 | 不適用。 |

## <a name="bad-memory-functions"></a>錯誤的記憶體函數

| 函式 | 描述 |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | 使用 [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) 函式註冊的應用程式定義函式，當偵測到一或多個錯誤的記憶體頁面時，便會呼叫此函數。 |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | 取得系統的記憶體錯誤處理功能。 |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | 註冊當偵測到一或多個錯誤的記憶體頁面時，所呼叫的錯誤記憶體通知。 |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | 關閉指定的錯誤記憶體通知控制碼。 |

## <a name="enclave-functions"></a>記憶體保護區函式

| 函式 | 描述 |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | 建立新的未初始化記憶體保護區。 記憶體保護區是程式碼的隔離區域，以及應用程式位址空間內的資料。 只有在記憶體保護區中執行的程式碼可以存取相同記憶體保護區內的資料。 |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | 初始化您建立並載入資料的記憶體保護區。 |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | 抓取是否支援指定的記憶體保護區類型。 |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | 將資料載入您藉由呼叫 [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)所建立的未初始化記憶體保護區。 |

## <a name="atl-thunk-functions"></a>ATL Thunk 函數

| 函式 | 描述 |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | 為 ATL Thunk 配置記憶體中的空間。 |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | 傳回對應于 AtlThunkData_t 參數的可執行函式。 |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | 釋放與 ATL Thunk 相關聯的記憶體。 |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | 初始化 ATL Thunk。 |

## <a name="obsolete-functions"></a>過時的函式

這些函式僅提供給 Windows 16 位版本的相容性：

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

下列函式可能會傳回不正確的資訊，不應使用此功能。 請改用 [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) 函數。

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)