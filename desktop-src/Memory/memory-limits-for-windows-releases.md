---
description: 本主題說明支援 Windows 和 Windows Server 版本的記憶體限制。
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Windows 與 Windows Server 版本的記憶體限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d2b11b636fcbcd3338986aa4ce88388f3b722045eee895e4acb1b62d5920eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992750"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Windows 與 Windows Server 版本的記憶體限制

本主題說明支援 Windows 和 Windows Server 版本的記憶體限制。

-   [記憶體和位址空間限制](#memory-limits-for-windows-and-windows-server-releases)
-   [實體記憶體限制： Windows 10](#physical-memory-limits-windows-10)
-   [實體記憶體限制： Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [實體記憶體限制： Windows 8](#physical-memory-limits-windows-8)
-   [實體記憶體限制： Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [實體記憶體限制： Windows 7](#physical-memory-limits-windows-7)
-   [實體記憶體限制： Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [實體記憶體限制： Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [實體記憶體限制： Windows Vista](#physical-memory-limits-windows-vista)
-   [實體記憶體限制： Windows Home Server](#physical-memory-limits-windows-home-server)
-   [實體記憶體限制： Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [實體記憶體限制： Windows Server 2003 （含 Service Pack 2） (SP2) ](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [實體記憶體限制： Windows Server 2003 （含 Service Pack 1） (SP1) ](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [實體記憶體限制： Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [實體記憶體限制： Windows XP](#physical-memory-limits-windows-xp)
-   [實體記憶體限制： Windows 內嵌](#physical-memory-limits-windows-embedded)
-   [圖形卡和其他裝置如何影響記憶體限制](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [相關主題](#related-topics)

記憶體和位址空間的限制會因平臺、作業系統，以及已 [**載入 \_ 映射**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)結構的 **圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知** 值，以及是否正在使用 [4 gb 調整](4-gigabyte-tuning.md) (4gt) 而有所不同。 **影像 \_使用/LARGEADDRESSAWARE 連結器選項設定或清除檔案 \_ 大型 \_ 位址 \_ 感知**。 [](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019)

4 gb 調整 (4GT) （也稱為應用程式記憶體微調或/3GB 參數）是一種技術 (只適用于32位系統) ，可改變使用者模式應用程式可用的虛擬位址空間數量。 啟用這項技術可減少系統虛擬位址空間的整體大小，因此系統資源上限。 如需詳細資訊，請參閱 [什麼是 4gt]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10))。

32位平臺的實體記憶體限制也取決於[實體位址延伸](physical-address-extension.md) (PAE) ，可讓32位 Windows 系統使用超過 4 GB 的實體記憶體。

## <a name="memory-and-address-space-limits"></a>記憶體和位址空間限制

下錶針對支援的 Windows 版本指定記憶體和位址空間的限制。 除非另有說明，否則此表中的限制適用于所有支援的版本。



| 記憶體類型                                                                                   | X86 的限制                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 64位 Windows 的限制                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 每個32位進程的使用者模式虛擬位址空間<br/>                            | 2 GB<br/> **圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知** 和4gt 最多 3 GB<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 具有 **影像檔案 \_ \_ 大型 \_ 位址 \_ 感知** 的 2 GB (預設) <br/> 具有 **影像檔案 \_ \_ 大型 \_ 位址 \_ 感知** 設定的 4 GB<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| 每個64位進程的使用者模式虛擬位址空間<br/>                            | 不適用<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **使用影像 \_檔案 \_ 大型 \_ 位址 \_ 感知** 集 (預設) ：<br/> **x64： Windows 8.1 和 Windows Server 2012 R2 或更新版本：** 128 TB<br/> **x64： Windows 8 和 Windows Server 2012 或較早的** 8 TB<br/> **Intel Itanium 型系統：** 7 TB<br/> <br/> 有 2 GB，已清除 **圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**<br/>                                                                                                                                                                                              |
| 核心模式虛擬位址空間<br/>                                                  | 2 GB<br/> 從 1 GB 到最多 2 GB （含4GT）<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 和 Windows Server 2012 R2 或更新版本：** 128 TB<br/> **Windows 8 和 Windows Server 2012 或更早的** 8 TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 分頁集區<br/>                                                                         | 384 GB 或系統認可限制，以較小者為准。 **Windows 8.1 和 Windows Server 2012 R2：** 15.5 TB 或系統認可限制，以較小者為准。 <br/> **Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 受到可用核心模式虛擬位址空間的限制。 從 Windows Vista Service Pack 1 (SP1) 開始，分頁集區也會受到[PagedPoolLimit](memory-management-registry-keys.md)登錄機碼值的限制。<br/> **Windows Home Server 和 Windows Server 2003：** 530 MB<br/> **Windows XP：** 490 MB<br/> <br/>                                                                                                 | 384 GB 或系統認可限制，以較小的 **Windows 8.1 和 Windows Server 2012 R2：** 15.5 TB 或系統認可限制（以較小者為准）。 <br/> **Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista：** 128 GB 或系統認可限制，以較小者為准<br/> **Windows Server 2003 和 Windows XP：** 取決於設定和 RAM 的最高 128 GB。<br/> <br/>                                                                                |
| 非分頁集區<br/>                                                                      | 75% 的 RAM 或 2 GB，以較小者為准。 **Windows 8.1 和 Windows Server 2012 R2：** RAM 或 16 TB，以較小的 (位址空間限制為 2 x RAM) 。<br/> **Windows Vista：** 僅受限於核心模式的虛擬位址空間和實體記憶體。 從 Windows Vista SP1 開始，非分頁集區也可以受到[NonPagedPoolLimit](memory-management-registry-keys.md)登錄機碼值的限制。<br/> **Windows Home Server、Windows Server 2003 和 Windows XP：** 256 MB，或具有 4 gb 的 128 MB。<br/> <br/>                                                                                                                                                 | RAM 或 128 GB （以較小的 (位址空間限制為 2 x ram) **Windows 8.1 和 Windows Server 2012 R2：** RAM 或 16 TB，以較小的 (位址空間限制為 2 x ram) 。<br/> **Windows server 2008 R2、Windows 7 和 Windows Server 2008：** 75% 的 RAM，最大為 128 GB<br/> **Windows Vista：** RAM 的40%，最高可達 128 GB。<br/> **Windows Server 2003 和 Windows XP：** 取決於設定和 RAM 的最高 128 GB。<br/> <br/> |
| 系統快取虛擬位址空間 (實體大小僅受限於實體記憶體) <br/> | 受限於可用的核心模式虛擬位址空間或 [SystemCacheLimit](memory-management-registry-keys.md) 登錄機碼值。<br/> **Windows 8.1 和 Windows Server 2012 R2：** 16 TB。<br/> **Windows Vista：** 僅受核心模式虛擬位址空間的限制。 從 Windows Vista SP1 開始，系統快取虛擬位址空間也會受到[SystemCacheLimit](memory-management-registry-keys.md)登錄機碼值的限制。<br/> **Windows Home Server、Windows Server 2003 和 Windows XP：** 860 MB，並設定 [LargeSystemCache](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10))登錄機碼，但不含 4gt;最高 448 MB 的 4 MB。<br/> <br/> | 無論實體 RAM **Windows 8.1 和 Windows Server 2012 R2：** 16 tb，一律為 1 TB。<br/> **Windows Server 2003 和 Windows XP：** 取決於設定和 RAM 的最高 1 TB。<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>實體記憶體限制： Windows 10

下表指定 Windows 10 實體記憶體的限制。



| 版本               | X86 的限制    | X64 的限制     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 工作站專業版  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>實體記憶體限制： Windows Server 2016

下表指定 Windows Server 2016 實體記憶體的限制。



| 版本                        | X64 的限制     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>實體記憶體限制： Windows 8

下表指定 Windows 8 實體記憶體的限制。



| 版本                | X86 的限制    | X64 的限制      |
|------------------------|-----------------|-------------------|
| Windows 8 企業版   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 專業版 | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>實體記憶體限制： Windows Server 2012

下表指定 Windows Server 2012 實體記憶體的限制。 Windows Server 2012 僅適用于 X64 版。



| 版本                               | X64 的限制     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Windows Storage Server 2012 Workgroup | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>實體記憶體限制： Windows 7

下表指定 Windows 7 之實體記憶體的限制。



| 版本                | X86 的限制    | X64 的限制      |
|------------------------|-----------------|-------------------|
| Windows 7 旗艦版     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 家用進階版 | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 家用入門版   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 簡易版      | 2 GB<br/> | N/A<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>實體記憶體限制： Windows Server 2008 R2

下表指定 Windows Server 2008 R2 之實體記憶體的限制。 Windows只有在64位版本中才提供 Server 2008 R2。



| 版本                                          | X64 的限制      | IA64 的限制   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| 適用於 Itanium 型系統的 Windows Server 2008 R2 |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>實體記憶體限制： Windows Server 2008

下表指定 Windows Server 2008 的實體記憶體限制。 32位的限制大於 4 GB Windows 假設已啟用[PAE](physical-address-extension.md) 。



| 版本                                       | X86 的限制     | X64 的限制      | IA64 的限制   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 for Itanium-Based Systems |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>實體記憶體限制： Windows Vista

下表指定 Windows Vista 之實體記憶體的限制。



| 版本                    | X86 的限制    | X64 的限制      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>實體記憶體限制： Windows Home Server

WindowsHome Server 僅適用于32位版本。 實體記憶體限制為 4 GB。

## <a name="physical-memory-limits-windows-server-2003-r2"></a>實體記憶體限制： Windows Server 2003 R2

下表指定 Windows Server 2003 R2 之實體記憶體的限制。 32位的限制超過 4 GB Windows 假設已啟用[PAE](physical-address-extension.md) 。



| 版本                                              | X86 的限制                                 | X64 的限制     |
|------------------------------------------------------|----------------------------------------------|------------------|
| WindowsServer 2003 R2 Datacenter Edition<br/> | 64 GB<br/>  (16 GB 加上 4GT) <br/> | 1 TB<br/>  |
| WindowsServer 2003 R2 Enterprise Edition<br/> | 64 GB<br/>  (16 GB 加上 4GT) <br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>實體記憶體限制： Windows Server 2003 （含 Service Pack 2） (SP2) 

下表指定 Windows Server 2003 Service Pack 2 (SP2) 的實體記憶體限制。 32位的限制超過 4 GB Windows 假設已啟用[PAE](physical-address-extension.md) 。



| 版本                                                                      | X86 的限制                                 | X64 的限制     | IA64 的限制   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| WindowsServer 2003 （含 Service Pack 2） (SP2) Datacenter Edition<br/> | 64 GB<br/>  (16 GB 加上 4GT) <br/> | 1 TB<br/>  | 2 TB<br/> |
| WindowsServer 2003 Service Pack 2 (SP2) 、Enterprise Edition<br/> | 64 GB<br/>  (16 GB 加上 4GT) <br/> | 1 TB<br/>  | 2 TB<br/> |
| WindowsServer 2003 Service Pack 2 (SP2) 、Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>實體記憶體限制： Windows Server 2003 （含 Service Pack 1） (SP1) 

下表指定 Windows Server 2003 Service Pack 1 (SP1) 之實體記憶體的限制。 32位的限制超過 4 GB Windows 假設已啟用[PAE](physical-address-extension.md) 。



| 版本                                                                      | X86 的限制                                 | X64 的限制        | IA64 的限制   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| WindowsServer 2003 （含 Service Pack 1） (SP1) Datacenter Edition<br/> | 64 GB<br/>  (16 GB 加上 4GT) <br/> | X64 1 TB<br/> | 1 TB<br/> |
| WindowsServer 2003 Service Pack 1 (SP1) 、Enterprise Edition<br/> | 64 GB<br/>  (16 GB 加上 4GT) <br/> | X64 1 TB<br/> | 1 TB<br/> |
| WindowsServer 2003 Service Pack 1 (SP1) 、Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>實體記憶體限制： Windows Server 2003

下表指定 Windows Server 2003 的實體記憶體限制。 32位的限制超過 4 GB Windows 假設已啟用[PAE](physical-address-extension.md) 。



| 版本                                                    | X86 的限制                                 | IA64 的限制     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003, Datacenter Edition<br/>         | 64 GB<br/>  (16 GB 加上 4GT) <br/> | 512 GB<br/> |
| Windows Server 2003, Enterprise Edition<br/>         | 64 GB<br/>  (16 GB 加上 4GT) <br/> | 512 GB<br/> |
| Windows Server 2003 Standard Edition<br/>           | 4 GB<br/>                              |                   |
| WindowsServer 2003，Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows 儲存體 Server 2003，Enterprise Edition<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>實體記憶體限制： Windows XP

下表指定 Windows XP 的實體記憶體限制。



| 版本                    | X86 的限制      | X64 的限制      | IA64 的限制                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 不支援 128 GB () <br/> |
| Windows XP Starter Edition | 512 MB<br/> | N/A<br/>    | N/A<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>實體記憶體限制： Windows 內嵌

下表指定 Windows 內嵌之實體記憶體的限制。



| 版本                                   | X86 的限制    | X64 的限制      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>圖形卡和其他裝置如何影響記憶體限制

裝置必須將記憶體對應至 4 GB 以下，以與非 PAE 感知的 Windows 版本相容。 因此，如果系統具有 4 GB 的 RAM，其中有些可能會被停用，或由 BIOS 重新對應到4GB 以上。 如果重新對應記憶體，X64 Windows 可以使用此記憶體。 X86 用戶端版本的 Windows 不支援超過 4 gb 的實體記憶體，因此無法存取這些重新對應的區域。 任何 X64 Windows 或 X86 伺服器版本都可以。

啟用 PAE 的 X86 用戶端版本具有可用的37位 (128 GB) 實體位址空間。 這些版本所強加的限制為最高允許的實體 RAM 位址，而不是 IO 空間的大小。 這表示，以 PAE 為感知的驅動程式可以實際使用超過 4 GB 的實體空間（如果需要的話）。 例如，驅動程式可以將位於 4 GB 以上的「遺失」記憶體區域對應，並將此記憶體公開為 RAM 磁碟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[4 gb 調整](4-gigabyte-tuning.md)
</dt> <dt>

[**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[實體位址擴充功能](physical-address-extension.md)
</dt> </dl>

 

 
