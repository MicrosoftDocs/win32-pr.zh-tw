---
description: 顯示如何使用 VSS 介面建立 VSS 硬體提供者。
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: VssSampleProvider 工具和範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd84288f6dc878c103f639aa0c015a3e5e95bde
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884414"
---
# <a name="vsssampleprovider-tool-and-sample"></a>VssSampleProvider 工具和範例

顯示如何使用 VSS [介面](volume-shadow-copy-api-interfaces.md) 建立 vss 硬體提供者。

> [!Note]  
> Microsoft Windows 軟體開發套件 (SDK) 包含 VssSampleProvider 工具和範例。 您可以從[適用于 Windows 8 的 Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/windows-8-sdk)下載 Windows SDK。

 

在 Windows SDK 安裝中，您可以 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (在64位 Windows) 和 (32 位 Windows) 中找到 VssSampleProvider 工具 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 。

> [!Note]  
> 只有 Windows Server 作業系統支援硬體提供者。 在 Windows 用戶端作業系統上，您可以編譯 VssSampleProvider 範例，但無法將它註冊為硬體提供者。

 

VssSampleProvider 工具組含下列檔案：

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

VssSampleProvider 範例包含下列安裝和卸載腳本：

-   Install-sampleprovider .cmd
-   Uninstall-sampleprovider .cmd
-   註冊 \_app.vbs

**安裝和使用 VssSampleProvider 範例**

1.  瀏覽至 `Program Files (x86)\Windows Kits\8.0\bin\` 目錄。 此目錄包含 virtualstoragevss.sys 和 vstorcontrol.exe。
2.  在指定的目錄中開啟命令提示字元視窗。
3.  若要安裝虛擬儲存驅動程式，請在 [命令提示字元] 視窗中輸入下列命令：

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  若要安裝 VSS 範例提供者，請在 [命令提示字元] 視窗中輸入下列命令：

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  若要建立虛擬 LUN，請執行下列動作。

    1.  在命令提示字元視窗中，鍵入下列命令：

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        此命令會建立虛擬 LUN，其儲存體識別碼為 **VSS 範例 HW 提供者**。 若要建立其他虛擬 Lun，請重複此步驟。

        只有當 **Vss 範例 HW 提供者** 是儲存體識別碼的一部分時，vss 範例提供者才會辨識 LUN。 如需儲存體識別碼的詳細資訊，請參閱下列 blog 文章。

        [LUN-使用 Diskshadow 和虛擬儲存體重新同步](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  在 [命令提示字元] 視窗中，使用 diskpart.exe 來格式化虛擬磁片並指派磁碟機號給它。

        以下是要在 diskpart 命令提示字元執行的範例腳本。

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  若要執行範例提供者，請在 [命令提示字元] 視窗中輸入下列命令：

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *&lt; 磁片 &gt; 磁碟機* 代表虛擬 LUN 的磁碟機號。

7.  若要卸載 VSS 範例提供者，請在 [命令提示字元] 視窗中輸入下列命令：

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  若要卸載虛擬儲存驅動程式，請在 [命令提示字元] 視窗中輸入下列命令：

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



