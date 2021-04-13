---
description: 開發您自己的 VSS 應用程式時，您應該觀察下列指導方針和限制。
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: VSS 應用程式相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318408"
---
# <a name="vss-application-compatibility"></a>VSS 應用程式相容性

開發您自己的 VSS 應用程式時，您應該觀察下列指導方針和限制。 您可能會發現，您可以參考 Microsoft Windows 軟體開發套件 (SDK) 中提供的 VSS 要求者、提供者和寫入器的範例程式碼。

> [!Note]  
> Windows SDK 僅適用于 Windows Vista 和更新版本的 Windows 作業系統版本，可用於開發 VSS 應用程式。 它無法用來開發 Windows Server 2003 R2、Windows Server 2003 或 Windows XP 的 VSS 要求者、提供者或寫入器。

 

**Windows server 2003 R2、Windows server 2003 和 WINDOWS XP：** 您可以從磁碟區陰影複製服務 7.2 SDK 取得 VSS，以供下載 [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) 。 請注意，Win2003 Obj 目錄下目錄中的64位 vssapi .lib 檔案 \\ 可用於64位版本的 Windows server 2003 R2、Windows server 2003 和 WINDOWS XP。 此 SDK 也提供 VSS 要求者、提供者和寫入器的範例程式碼。

## <a name="compiling-vss-applications"></a>編譯 VSS 應用程式

開發要求者時，例如備份應用程式：

-   包含下列標頭： <dl> Vss。h  
    VsWriter。h  
    VsBackup。h  
    </dl>
-   Link the following library: <dl> VssApi .Lib  
    </dl>

開發寫入器時：

-   包含下列標頭： <dl> Vss。h  
    VsWriter。h  
    </dl>
-   Link the following library: <dl> VssApi .lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>支援的設定和限制

下列清單說明支援的設定和限制：

-   從 Windows XP 開始的 Windows 作業系統版本會提供並支援 VSS。
-   下表摘要說明 Windows 版本之間的相容性資訊。 請注意，如果 VSS 應用程式「已針對」指定的 Windows 版本進行編譯，這表示應用程式是使用該版本專用的標頭檔和程式庫進行編譯。

    > [!Note]  
    > 硬體提供者只會在 Windows server 作業系統版本上執行。 它們不會在 Windows 用戶端作業系統版本上執行。

     

    > [!Note]  
    > 在下表中，Windows Server 2008 （含 Service Pack 2 (SP2) 應視為與 Windows Server 2008 相同。 如需 Windows Server 2008 （含 SP2）的詳細資訊，請參閱 <https://go.microsoft.com/fwlink/p/?linkid=178730> 。 Windows Server 2003 R2 應視為與 Windows Server 2003 相同。

     

    > [!Note]  
    > 如果針對 Windows Server 2003 或更新版本編譯 VSS 應用程式，它也會在較新版本的 Windows 上執行。

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>為其編譯的 VSS 要求者、寫入器和提供者</th>
    <th>將執行于</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Windows Server 2008 R2 (64 位) 、Windows 7 (64 位) 、Windows Server 2008 (64 位) 和 Windows Vista (64 位) </td>
    <td>Windows Server 2008 R2 (64 位) 、Windows 7 (64 位) 、Windows Server 2008 (64 位) 和 Windows Vista (64 位) </td>
    </tr>
    <tr class="even">
    <td>Windows Server 2008 R2 (32 位) 、Windows 7 (32 位) 、Windows Server 2008 (32 位) 和 Windows Vista (32 位) </td>
    <td>Windows Server 2008 R2 (32 位) 、Windows 7 (32 位) 、Windows Server 2008 (32 位) 和 Windows Vista (32 位) </td>
    </tr>
    <tr class="odd">
    <td>Windows Server 2003 (64 位元)</td>
    <td>Windows Server 2008 R2 (64 位) 、Windows 7 (64 位) 、Windows Server 2008 (64 位) 、Windows Vista (64 位) ，以及 Windows Server 2003 (64 位) </td>
    </tr>
    <tr class="even">
    <td>Windows Server 2003 (32 位元)</td>
    <td>Windows Server 2008 R2 (32 位) 、Windows 7 (32 位) 、Windows Server 2008 (32 位) 、Windows Vista (32 位) ，以及 Windows Server 2003 (32 位)  <blockquote>
    [!Note]<br />
要求者也會在 Windows Server 2003 (64 位) 上執行。
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>Windows XP 64 位版本</td>
    <td>Windows Server 2003 (64 位) 和 Windows XP 64 位版本</td>
    </tr>
    <tr class="even">
    <td>Windows XP (32 位元)</td>
    <td>Windows XP (32 位元)</td>
    </tr>
    </tbody>
    </table>

    

     

    

    | 編譯 VSS 要求者、寫入器或提供者        | 使用                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 或 Windows 7                        | Windows 7 (的 Windows SDK 可從 [Windows 下載中心](https://www.microsoft.com/download/details.aspx?id=8279)取得。 )                 |
    | Windows Server 2008 或 Windows Vista                       | Windows SDK Windows Server 2008 (可從 [Windows SDK 開發人員中心](https://msdn.microsoft.com/windows/bb980924.aspx)取得。 )  |
    | Windows Server 2003 R2、Windows Server 2003 或 Windows XP | [磁碟區陰影複製服務 7.2 SDK](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   所有32位 VSS 應用程式 (要求者、提供者和寫入器) 必須以原生32位或64位應用程式的形式執行。 不支援在 WOW64 下執行它們。

    **Windows Server 2003 和 WINDOWS XP：** 支援在 WOW64 下執行32位 VSS 要求者，但不支援系統狀態備份。 不支援在 WOW64 下執行32位 VSS 提供者和寫入器。 在 Windows Vista 和後續版本中，已移除在 WOW64 下執行32位要求者的支援。

-   在 Windows Server 2003 R2 或 Windows Server 2003 上建立的陰影複製，無法在執行 Windows Server 2008 R2 或 Windows Server 2008 的電腦上使用。 在 Windows Server 2008 R2 或 Windows Server 2008 上建立的陰影複製無法在執行 Windows Server 2003 的電腦上使用。 不過，在 Windows Server 2008 上建立的陰影複製可以在執行 Windows Server 2008 R2 的電腦上使用，反之亦然。
-   若要支援陰影複製，執行 VSS 的系統必須至少有一個 NTFS 檔案系統。 此檔案系統將裝載陰影複製的「差異區域」。 如需詳細資訊，請參閱 [系統提供者](providers.md)。
-   假設有一個 NTFS 檔案系統，並提供適當的內容選擇 (請參閱 [陰影複製內容](shadow-copy-context-configurations.md) 設定) ，任何支援的本機檔案系統都可進行陰影複製。
-   您只能針對本機掛接的檔案系統製作陰影複製。 裝載遠端共用和其他跨掛接檔案系統的系統無法進行陰影複製。 這些檔案系統只能由提供檔案系統的系統進行陰影複製。
-   寫入器和要求者只能指定本機資源。 本機資源是一組檔案，其絕對路徑開頭為磁碟機號，而磁碟機號無法與遠端共用上掛接的資料夾相關聯。
-   每個磁片區的軟體陰影複製數目上限為512。 不過，根據預設，您只能維護 64 個「共用資料夾陰影複製」功能所使用的陰影複製。 若要變更共用資料夾陰影複製功能的限制，請使用 [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) 登錄機碼。
-   備份元件基礎結構不支援將叢集資源備份為寫入器元件。 若要備份叢集資源，應用程式應該假設路徑是指定特定叢集節點的本機路徑。
-   [!Note]  
    > Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。

     

    備份和復原系統狀態時，建議的策略是除了系統狀態寫入器所列舉的檔案之外，還會備份和復原系統和開機磁碟區。

    > [!Note]  
    > 系統狀態寫入器是將 [ [**vss \_ 使用 \_ 類型**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) ] 屬性設為 [vss \_ BOOTABLESYSTEMSTATE] 或 [ \_ vss SYSTEMSERVICE] 的寫入器 \_ \_ 。

     

 

 
