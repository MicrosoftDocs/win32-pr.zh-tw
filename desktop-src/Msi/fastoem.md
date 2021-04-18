---
description: FASTOEM 屬性的設計目的是要讓 Oem 縮短為特定案例安裝 Windows Installer 應用程式所需的時間。
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976251"
---
# <a name="fastoem-property"></a>FASTOEM 屬性

**FASTOEM** 屬性的設計目的是要讓 oem 縮短為特定案例安裝 Windows Installer 應用程式所需的時間。 請勿將 **FASTOEM** 屬性撰寫至 [屬性資料表](property-table.md)。

只有在下列所有條件都成立時，才適用 **FASTOEM** 屬性：

-   應用程式會安裝在與包含原始程式檔的資料夾相同的磁片區上。
-   系統會在安裝後刪除來源檔案。
-   安裝期間不會顯示任何使用者介面。 [使用者介面層級](user-interface-levels.md)為 [無]。
-   安裝會在每一電腦的 [安裝內容](installation-context.md)中執行。
-   電腦上有足夠的空間可順利安裝。
-   這是第一次安裝。 安裝未公告、重新安裝、移除或執行系統管理安裝。
-   未安裝任何功能以從來源執行。
-   安裝套件未包含任何 [獨立元件](isolated-components.md)。 因為隔離的元件需要來源檔案保持在來源，所以 **FASTOEM** 屬性目前無法與隔離的元件一起使用。

如果上述所有條件都成立，則設定 **FASTOEM** 屬性可讓 Windows Installer 藉由執行下列動作來改善效能：

-   移動而不是複製相同磁片區上的檔案。 這並不保證會移動所有檔案，而不是複製。 請注意，如果電腦有多個硬碟，您必須將命令列上的 [**ROOTDRIVE**](rootdrive.md) 屬性初始化到包含安裝來源的相同磁片磁碟機。
-   從應用程式的來源清單中省略此來源，讓後續的重新安裝或維護安裝預設為 [媒體資料表](media-table.md)中指定的 cd-rom 來源。
-   簡化檔案 [成本](file-costing.md)。
-   隱藏從 Windows Installer 傳送至用戶端的進度訊息。

## <a name="remarks"></a>備註

由於設定 **FASTOEM** 時不會傳送任何進度訊息，因此建議作者手動將 Timeout 的1800值寫入至金鑰

**HKLM** \\**軟體** \\**原則** \\**Microsoft** \\**Windows** \\**安裝程式** \\**Timeout**

Timeout 是 **REG \_ DWORD** 型別。

若要在 Windows 2000 主控台的 [新增或移除程式] 中顯示應用程式大小，您必須手動將 EstimatedSize 的值寫入機碼

**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**卸載** \\**< *產品* 代碼 >**

這是 **REG \_ DWORD** 型別，等於應用程式大小（以 kb 為單位）。 安裝程式不會自動寫入此值。

如果傳送給終端使用者的 CD-ROM 將應用程式的安裝套件儲存在 CD-ROM 的根目錄，請使用下列範例命令列。 請注意，.msi 檔案的 [Media 資料表](media-table.md) 中的磁片區標籤必須與 cd-rom 的磁片區標籤相符。

**Msiexec/I C： \\ TempImage \\package.msi/qn/LE logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C：\\**

如果安裝套件不是位於傳送給使用者的 CD-ROM 根目錄，請使用下列範例命令列。 在此情況下，您必須將 [**MEDIAPACKAGEPATH**](mediapackagepath.md) 屬性設定為安裝套件的路徑。 .Msi 檔案的 [媒體資料表](media-table.md) 中的磁片區標籤必須符合 cd-rom 的磁片區標籤。 在此情況下，請遵循此範例。

**Msiexec/I C： \\ TempImage \\package.msi/qn/LE logfile.txt ALLUSERS = 1 FASTOEM = 1 DISABLEROLLBACK = 1 MEDIAPACKAGEPATH = C： \\ TempImage \\package.msi ROOTDRIVE = c：\\**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




