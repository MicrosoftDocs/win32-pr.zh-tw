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
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="76f44-104">在安裝期間隱藏 [取消] 按鈕</span><span class="sxs-lookup"><span data-stu-id="76f44-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="76f44-105">您可以使用命令列選項、Windows Installer API 或自訂動作來隱藏用來取消安裝的 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="76f44-106">您可以根據所使用的方法，隱藏部分或所有安裝的 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="76f44-107">從命令列隱藏 [取消] 按鈕</span><span class="sxs-lookup"><span data-stu-id="76f44-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="76f44-108">您可以使用 (！ ) 命令列選項，在安裝期間隱藏 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="76f44-109">這只能在基本使用者介面層級安裝 (/qb) 中完成。</span><span class="sxs-lookup"><span data-stu-id="76f44-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="76f44-110">整個安裝會隱藏 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="76f44-111">如需詳細資訊，請參閱 [命令列選項](command-line-options.md) 和 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="76f44-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="76f44-112">下列命令列將隱藏 [ **取消** ] 按鈕，並安裝 Example.msi。</span><span class="sxs-lookup"><span data-stu-id="76f44-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="76f44-113">**msiexec/I example.msi/qb！**</span><span class="sxs-lookup"><span data-stu-id="76f44-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="76f44-114">從應用程式或腳本隱藏 [取消] 按鈕</span><span class="sxs-lookup"><span data-stu-id="76f44-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="76f44-115">您可以撰寫應用程式或腳本來隱藏 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="76f44-116">這僅適用于基本的 UI 層級安裝，如此一來，整個安裝就會隱藏 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="76f44-117">若要從應用程式隱藏 [取消] 按鈕，請 \_ 在呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)時設定 INSTALLUILEVEL HIDECANCEL。</span><span class="sxs-lookup"><span data-stu-id="76f44-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="76f44-118">下列範例會隱藏 [ **取消** ] 按鈕，並安裝 Example.msi。</span><span class="sxs-lookup"><span data-stu-id="76f44-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


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



<span data-ttu-id="76f44-119">若要從腳本隱藏 [**取消**] 按鈕，請將 msiUILevelHideCancel 新增至 [**安裝程式物件**](installer-object.md)的 [**UILevel**](installer-uilevel.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="76f44-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="76f44-120">下列 VBScript 範例會隱藏 [ **取消** ] 按鈕，並安裝 Example.msi。</span><span class="sxs-lookup"><span data-stu-id="76f44-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="76f44-121">使用自訂動作隱藏部分安裝部分的 [取消] 按鈕</span><span class="sxs-lookup"><span data-stu-id="76f44-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="76f44-122">安裝過程中，您可以 \_ 使用 DLL 自訂動作或腳本來傳送 INSTALLMESSAGE COMMONDATA 訊息，以隱藏和取消隱藏安裝元件中的 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="76f44-123">如需詳細資訊，請參閱 [動態連結程式庫](dynamic-link-libraries.md)、 [腳本](scripts.md)、 [自訂動作](custom-actions.md)，以及 [使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。</span><span class="sxs-lookup"><span data-stu-id="76f44-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="76f44-124">自訂動作的呼叫必須提供記錄。</span><span class="sxs-lookup"><span data-stu-id="76f44-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="76f44-125">此記錄的欄位1必須包含值 2 (兩個) 來指定 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="76f44-126">欄位2必須包含值0或1。</span><span class="sxs-lookup"><span data-stu-id="76f44-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="76f44-127">欄位2中的0值會隱藏按鈕，而欄位2中的值為1會 unhides 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="76f44-128">請注意，使用 [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) 配置大小2的記錄，會提供欄位0、1和2。</span><span class="sxs-lookup"><span data-stu-id="76f44-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="76f44-129">下列範例 DLL 自訂動作會隱藏 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


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



<span data-ttu-id="76f44-130">下列 VBScript 自訂動作會隱藏 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="76f44-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


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



 

 



