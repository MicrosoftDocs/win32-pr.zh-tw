---
description: 實體位址延伸 (PAE) 是一種處理器功能，可讓 x86 處理器存取超過 4 GB 的可用 Windows 版本實體記憶體。
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: 實體位址擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027571"
---
# <a name="physical-address-extension"></a>實體位址擴充功能

實體位址延伸 (PAE) 是一種處理器功能，可讓 x86 處理器存取超過 4 GB 的可用 Windows 版本實體記憶體。 在 x86 系統上執行的某些32位版本的 Windows Server，可以使用 PAE 來存取高達 64 GB 或 128 GB 的實體記憶體，視處理器的實體位址大小而定。 如需詳細資訊，請參閱 [Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)。

Intel Itanium 和 x64 處理器架構可以原生存取超過 4 GB 的實體記憶體，因此不會提供對等的 PAE。 只有在 x86 系統上執行的32位版本的 Windows 才會使用 PAE。

使用 PAE 時，作業系統會從兩個層級的線性位址轉譯移到三層的位址轉譯。 它不會將線性位址分割成三個不同的欄位來編制記憶體資料表的索引，而是將其分割成四個不同的欄位：2位位欄位、2 9 位位欄位和12位位位，其對應于 Intel 架構 (4 KB) 所執行的頁面大小。 在 PAE 模式下，頁面資料表專案的大小 (Pte) 和 (PDEs) 的頁面目錄專案會從32增加至64位。 額外的位可讓作業系統 PTE 或 PDE 參考超過 4 GB 的實體記憶體。

在以 x64 為基礎的系統上執行的32位 Windows 中，PAE 也啟用了數種先進的系統和處理器功能，包括支援硬體的 [資料執行防止](data-execution-prevention.md) (DEP) 、 [非統一記憶體存取 (NUMA) ](../procthread/numa-support.md)，以及在執行 (熱新增記憶體) 的情況下，將記憶體新增至系統的功能。

PAE 不會變更進程可用的虛擬位址空間數量。 在32位視窗中執行的每個進程仍然受限於 4 GB 的虛擬位址空間。

## <a name="system-support-for-pae"></a>適用于 PAE 的系統支援

只有在下列以 x86 為基礎的系統上執行的 Windows 32 位版本上，才支援 PAE：

-   Windows 7 (僅限32位) 
-   Windows Server 2008 (僅限32位) 
-   Windows Vista (僅限32位) 
-   Windows Server 2003 (僅限32位) 
-   僅限 Windows XP (32 位) 

## <a name="enabling-pae"></a>啟用 PAE

如果已在支援啟用硬體 DEP 的電腦上啟用 DEP，或電腦已設定為在超過 4 GB 的記憶體範圍內熱新增記憶體裝置，則 Windows 會自動啟用 PAE。 如果電腦不支援已啟用硬體的 DEP，或未針對記憶體範圍中的熱新增記憶體裝置設定超過 4 GB，則必須明確地啟用 PAE。

若要明確啟用 PAE，請使用下列 [**BCDEdit/set**](/windows-hardware/drivers/devtest/bcdedit--set) 命令設定 **pae** 開機專案選項：

 **bcdedit/set \[ {ID} \] pae ForceEnable**  


如果已啟用 DEP，則無法停用 PAE。 使用下列 [**BCDEdit/set**](/windows-hardware/drivers/devtest/bcdedit--set) 命令來停用 DEP 和 PAE：

 **bcdedit/set \[ {ID} \] nx AlwaysOff**  
**bcdedit/set \[ {ID} \] pae ForceDisable**  


**Windows Server 2003 和 WINDOWS XP：** 若要啟用 PAE，請使用 [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file)檔案中的 **/pae** 參數。 若要停用 PAE，請使用 **/NOPAE** 參數。 若要停用 DEP，請使用 **/EXECUTE** 參數。

## <a name="comparing-pae-and-other-large-memory-support"></a>比較 PAE 和其他海量儲存體支援

PAE、 [4 gb 調整](4-gigabyte-tuning.md) (4gt) ，以及 [定址視窗擴充](address-windowing-extensions.md) (AWE) 提供不同的用途，並可獨立使用：

-   PAE 可讓作業系統存取及使用超過 4 GB 的實體記憶體。
-   4GT 可將進程可用的虛擬位址空間部分從 2 GB 增加至最多 3 GB。
-   AWE 是一組 Api，可讓處理常式配置未分頁的實體記憶體，然後將此記憶體的部分動態對應到進程的虛擬位址空間中。

如果沒有使用4GT 或 AWE，單一32位進程可使用的實體記憶體數量受限於 (2 GB) 的位址空間大小。 在此情況下，啟用 PAE 的系統仍可使用超過 4 GB 的 RAM，同時執行多個進程或將檔案資料快取到記憶體中。

您可以搭配或不使用 PAE 來使用4GT。 不過，某些版本的 Windows 會限制使用4GT 時可支援的實體記憶體數量上限。 在這類系統上，以4GT 啟用開機會導致作業系統略過超過限制的記憶體。

AWE 不需要 PAE 或4GT，但通常會與 PAE 一起使用，從單一32位進程配置超過 4 GB 的實體記憶體。

## <a name="related-topics"></a>相關主題



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[PAE X86 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
