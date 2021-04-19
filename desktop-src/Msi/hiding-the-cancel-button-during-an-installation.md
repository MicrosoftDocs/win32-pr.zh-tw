---
description: 您可以使用命令列選項、Windows Installer API 或自訂動作來隱藏用來取消安裝的 [取消] 按鈕。 您可以根據所使用的方法，隱藏部分或所有安裝的 [取消] 按鈕。
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: 在安裝期間隱藏 [取消] 按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975160"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a>在安裝期間隱藏 [取消] 按鈕

您可以使用命令列選項、Windows Installer API 或自訂動作來隱藏用來取消安裝的 [ **取消** ] 按鈕。 您可以根據所使用的方法，隱藏部分或所有安裝的 [ **取消** ] 按鈕。

## <a name="hiding-the-cancel-button-from-the-command-line"></a>從命令列隱藏 [取消] 按鈕

您可以使用 (！ ) 命令列選項，在安裝期間隱藏 [ **取消** ] 按鈕。 這只能在基本使用者介面層級安裝 (/qb) 中完成。 整個安裝會隱藏 [ **取消** ] 按鈕。 如需詳細資訊，請參閱 [命令列選項](command-line-options.md) 和 [消費者介面層級](user-interface-levels.md)。 下列命令列將隱藏 [ **取消** ] 按鈕，並安裝 Example.msi。

**msiexec/I example.msi/qb！**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>從應用程式或腳本隱藏 [取消] 按鈕

您可以撰寫應用程式或腳本來隱藏 [ **取消** ] 按鈕。 這僅適用于基本的 UI 層級安裝，如此一來，整個安裝就會隱藏 [ **取消** ] 按鈕。

若要從應用程式隱藏 [取消] 按鈕，請 \_ 在呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)時設定 INSTALLUILEVEL HIDECANCEL。 下列範例會隱藏 [ **取消** ] 按鈕，並安裝 Example.msi。


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



若要從腳本隱藏 [**取消**] 按鈕，請將 msiUILevelHideCancel 新增至 [**安裝程式物件**](installer-object.md)的 [**UILevel**](installer-uilevel.md)屬性。 下列 VBScript 範例會隱藏 [ **取消** ] 按鈕，並安裝 Example.msi。


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>使用自訂動作隱藏部分安裝部分的 [取消] 按鈕

安裝過程中，您可以 \_ 使用 DLL 自訂動作或腳本來傳送 INSTALLMESSAGE COMMONDATA 訊息，以隱藏和取消隱藏安裝元件中的 [取消] 按鈕。 如需詳細資訊，請參閱 [動態連結程式庫](dynamic-link-libraries.md)、 [腳本](scripts.md)、 [自訂動作](custom-actions.md)，以及 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。

自訂動作的呼叫必須提供記錄。 此記錄的欄位1必須包含值 2 (兩個) 來指定 [ **取消** ] 按鈕。 欄位2必須包含值0或1。 欄位2中的0值會隱藏按鈕，而欄位2中的值為1會 unhides 按鈕。 請注意，使用 [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) 配置大小2的記錄，會提供欄位0、1和2。

下列範例 DLL 自訂動作會隱藏 [ **取消** ] 按鈕。


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



下列 VBScript 自訂動作會隱藏 [ **取消** ] 按鈕。


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



