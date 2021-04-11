---
title: " (舊版 Windows 環境功能安裝和註冊通訊協定處理常式) "
description: 安裝通訊協定處理常式牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置並加以註冊。
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317083"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a> (舊版 Windows 環境功能安裝和註冊通訊協定處理常式) 

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

安裝 **通訊協定處理常式** 牽涉到將 DLL (s) 複製到 Program Files 目錄中的適當位置並加以註冊。

本節包含下列主題：

-   [安裝指導方針](#installation-guidelines)
-   [註冊通訊協定處理常式](#to-register-protocol-handlers)
-   [註冊 Shell 擴充功能](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>安裝指導方針

通訊協定處理常式應該執行自我註冊以進行安裝，並遵循下列指導方針：

-   安裝程式必須使用 EXE 或 MSI 安裝程式。
-   必須提供版本資訊。
-   每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。
-   安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。
-   如果先前的增益集遭到覆寫，安裝程式應通知使用者。
-   如果較新的增益集覆寫了先前的增益集，就應該能夠還原先前增益集的功能，並使它成為該檔案類型的預設增益集。

## <a name="to-register-protocol-handlers"></a>註冊通訊協定處理常式

您必須在登錄中建立14個專案，以註冊通訊協定處理常式元件，其中：

-   *Ver \_Ind \_ ProgID* 是通訊協定處理常式執行的獨立 ProgID 版本
-   *Ver \_Dep \_ ProgID* 是通訊協定處理常式執行的相依 ProgID 版本
-   *Clsid \_ 1* 是通訊協定處理常式執行的 clsid

1.  使用下列索引鍵和值註冊版本獨立 ProgID：

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  使用下列索引鍵和值註冊版本相依 ProgID：

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  使用下列索引鍵和值註冊通訊協定處理常式的 CLSID：

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  使用 Windows Desktop Search 註冊通訊協定處理常式：

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a>註冊 Shell 擴充功能

您必須在登錄中建立兩個專案，才能註冊通訊協定處理常式的 Shell 延伸模組。

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




