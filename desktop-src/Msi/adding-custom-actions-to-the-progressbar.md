---
description: 自訂動作可以將時間和進度資訊新增至 ProgressBar 控制項。 如需建立具有 ProgressBar 之動作顯示對話方塊的詳細資訊，請參閱撰寫 ProgressBar 控制項。
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: 將自訂動作新增至 ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d83dfeb806eb0ed6f1e251dd48b97911d8e0f583c8b65cb48ef0d04df059ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811058"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>將自訂動作新增至 ProgressBar

[自訂動作](custom-actions.md) 可以將時間和進度資訊新增至 [ProgressBar](progressbar-control.md) 控制項。 如需建立具有 ProgressBar 之動作顯示對話方塊的詳細資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)。

請注意，您必須將兩個自訂動作新增至 Windows Installer 套件，才能正確地將時間和進度資訊報告給 ProgressBar。 其中一個自訂動作必須是延後的自訂動作。 此自訂動作應完成您的自訂安裝，並在安裝程式執行安裝腳本時，將個別的增量數量傳送給 [ProgressBar](progressbar-control.md) 控制項。 第二個自訂動作必須是立即執行自訂動作，以在安裝的取得和腳本產生階段期間，通知 ProgressBar 要加總多少刻度。

**將自訂動作新增至 ProgressBar**

1.  決定自訂動作將如何描述其進度。 例如，安裝登錄機碼的自訂動作可能會顯示進度訊息，並在每次安裝程式寫入一個登錄機碼時更新 [ProgressBar](progressbar-control.md) 。
2.  自訂動作的每個更新都會以常數增量變更 [ProgressBar](progressbar-control.md) 的長度。 指定或計算每個增量中的刻度數目。 一般來說，一個刻度的 ProgressBar 長度變更會對應到一個位元組的安裝。 例如，如果安裝程式在寫入一個登錄機碼時安裝大約10000個位元組，您可以指定遞增中有10000個刻度。
3.  指定或計算自訂動作新增至 [ProgressBar](progressbar-control.md)長度的總刻度數。 自訂動作加入的刻度數目通常會計算為： (刻度遞增) x () 的專案數目。 例如，如果自訂動作寫入10個登錄機碼，安裝程式就會安裝大約100000個位元組，因此安裝程式必須增加 ProgressBar 最後總長度的估計值（依100000刻度）。
    > [!Note]  
    > 若要以動態方式計算，自訂動作必須包含在腳本產生期間立即執行的區段。 延後執行自訂動作所報告的刻度數量必須等於由立即執行動作新增至總滴答計數的刻度數目。 如果不是這種情況，TimeRemaining 文字控制項所報告的剩餘時間將會不正確。

     

4.  將自訂動作區分為兩個部分的程式碼：在腳本產生階段期間執行的區段，以及在安裝執行階段期間執行的區段。 您可以使用兩個檔案來執行這項作業，也可以透過在安裝程式的執行模式上進行調節來使用一個檔案。 下列範例會使用一個檔案並檢查安裝狀態。 範例的區段會根據安裝程式是否在安裝的執行或腳本產生階段，來執行。
5.  腳本產生期間執行的區段應該會增加 [ProgressBar](progressbar-control.md) 最後總長度的估計值（依自訂動作中的總刻度數）。 這是藉由傳送 **ProgressAddition** 進度訊息來完成。
6.  在安裝執行階段期間執行的區段應該設定郵件內文和範本，以通知使用者自訂動作的作用，以及指示安裝程式更新 [ProgressBar](progressbar-control.md) 控制項。 例如，通知安裝程式將 ProgressBar 向前移動一次，並使用每個更新傳送明確的進度訊息。 如果自訂動作正在安裝某個東西，此區段中通常會有一個迴圈。 每次通過此迴圈時，安裝程式都可以安裝一個參考專案，例如登錄機碼，並更新 ProgressBar 控制項
7.  將立即執行自訂動作新增至 Windows Installer 套件。 此自訂動作會通知 [ProgressBar](progressbar-control.md) 在安裝的取得和腳本產生階段期間，要進多少。 在下列範例中，來源是藉由編譯範例程式碼所建立的 DLL，而目標則是 CAProgress 的進入點。
8.  將順延強制自訂動作新增至 Windows Installer 套件。 此自訂動作會完成實際安裝的步驟，並在安裝程式執行安裝腳本時，通知 [ProgressBar](progressbar-control.md) 有多少可將長條前進。 在下列範例中，來源是藉由編譯範例程式碼所建立的 DLL，而目標則是 CAProgress 的進入點。
9.  在[InstallExecuteSequence](installexecutesequence-table.md)資料表的[InstallInitialize](installinitialize-action.md)和[InstallFinalize](installfinalize-action.md)之間，排程自訂動作。 延遲的自訂動作應該在立即執行自訂動作之後立即排程。 安裝程式在執行腳本之前，不會執行延遲的自訂動作。

下列範例會示範如何將自訂動作新增至 [ProgressBar](progressbar-control.md)。 這兩個自訂動作的來源都是藉由編譯範例程式碼所建立的 DLL，而這兩個自訂動作的目標是 CAProgress 的進入點。 這個範例不會對系統進行任何實際的變更，但會將 ProgressBar 的運作方式，就像是安裝10個以上大約10000個位元組大小的參考專案一樣。 安裝程式會在每次安裝參考專案時更新訊息和 ProgressBar。


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



