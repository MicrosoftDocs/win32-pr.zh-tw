---
description: 還原選項可讓要求者將自訂的還原選項傳達給寫入器。
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: 設定 VSS 還原選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980801"
---
# <a name="setting-vss-restore-options"></a>設定 VSS 還原選項

還原選項可讓要求者將自訂的還原選項傳達給寫入器。

## <a name="restore-options"></a>還原選項

將還原選項的格式標準化，可讓寫入器和要求者處理常見的自訂要求。 在呼叫 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)方法之前，會針對每個選取的備份元件呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)方法，以針對要求者設定還原選項。 在 *wszRestoreOptions* 參數中傳遞給 **SetRestoreOptions** 方法的字串可以包含多個值，如下所述。

## <a name="format"></a>格式

還原選項的格式為一或多個以逗號分隔的名稱/值組，而且名稱會選擇性地加上其所套用的子元件名稱。 元件名稱和選項名稱不區分大小寫。 值的區分大小寫取決於寫入器。 例如：

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

在此範例中，"Option1" 僅適用于 "Child1" 子元件和其子系，"Option2" 適用于所有元件及其下階，而 "Option3" 只適用于 "Child2 \\ Grandchild3" 子元件及其下階。

[**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)方法只能在可選取要進行備份的元件上呼叫，而子節點可能無法針對備份進行選取，它們可能可供還原。

## <a name="common-restore-options"></a>一般還原選項

這些常見的還原選項已定義為增加寫入器與要求者之間的互通性。

-   權威

    「授權」選項支援多個「專案」值，但只能有一個「全部」值。

    整個元件都具有授權。

    ``` syntax
    "Authoritative"="All"
    ```

    只有指定的專案具有授權。 命名專案的格式是由寫入器定義。 常見的指定是 " \* " 表示所有檔案，"..."表示指定元件的所有檔案和子目錄。

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   向前復原

    還原資料庫之後，寫入器通常會透過記錄向前復原，讓資料庫保持在最新狀態。 在增量或差異還原的情況下，要求者會使用 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) 方法來部分控制記錄處理行為，此還原選項可讓您更細微地控制。

    請勿變換記錄。

    ``` syntax
    "Roll Forward"="None"
    ```

    滾動所有記錄。

    ``` syntax
    "Roll Forward"="All"
    ```

    向前復原記錄到指定的時間點。 指定點的格式是由寫入器定義。

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   新元件名稱

    寫入器可能會想要將元件還原至新的名稱。 例如，將資料庫還原至不同的名稱來還原個別專案;還原為相同的名稱會讓所有資料都建議寫入器接受有效的邏輯路徑和元件名稱做為此選項的值。 這通常會與 [*導向的目標*](vssgloss-d.md)搭配使用。

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



