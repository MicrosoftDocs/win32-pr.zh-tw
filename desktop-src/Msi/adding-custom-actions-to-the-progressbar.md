---
description: 自訂動作可以將時間和進度資訊新增至 ProgressBar 控制項。 如需建立具有 ProgressBar 之動作顯示對話方塊的詳細資訊，請參閱撰寫 ProgressBar 控制項。
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: 將自訂動作新增至 ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977291"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="57ad8-104">將自訂動作新增至 ProgressBar</span><span class="sxs-lookup"><span data-stu-id="57ad8-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="57ad8-105">[自訂動作](custom-actions.md) 可以將時間和進度資訊新增至 [ProgressBar](progressbar-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="57ad8-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="57ad8-106">如需建立具有 ProgressBar 之動作顯示對話方塊的詳細資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)。</span><span class="sxs-lookup"><span data-stu-id="57ad8-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="57ad8-107">請注意，您必須將兩個自訂動作新增至 Windows Installer 套件，才能正確地將時間和進度資訊報告給 ProgressBar。</span><span class="sxs-lookup"><span data-stu-id="57ad8-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="57ad8-108">其中一個自訂動作必須是延後的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="57ad8-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="57ad8-109">此自訂動作應完成您的自訂安裝，並在安裝程式執行安裝腳本時，將個別的增量數量傳送給 [ProgressBar](progressbar-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="57ad8-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="57ad8-110">第二個自訂動作必須是立即執行自訂動作，以在安裝的取得和腳本產生階段期間，通知 ProgressBar 要加總多少刻度。</span><span class="sxs-lookup"><span data-stu-id="57ad8-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="57ad8-111">**將自訂動作新增至 ProgressBar**</span><span class="sxs-lookup"><span data-stu-id="57ad8-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="57ad8-112">決定自訂動作將如何描述其進度。</span><span class="sxs-lookup"><span data-stu-id="57ad8-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="57ad8-113">例如，安裝登錄機碼的自訂動作可能會顯示進度訊息，並在每次安裝程式寫入一個登錄機碼時更新 [ProgressBar](progressbar-control.md) 。</span><span class="sxs-lookup"><span data-stu-id="57ad8-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="57ad8-114">自訂動作的每個更新都會以常數增量變更 [ProgressBar](progressbar-control.md) 的長度。</span><span class="sxs-lookup"><span data-stu-id="57ad8-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="57ad8-115">指定或計算每個增量中的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="57ad8-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="57ad8-116">一般來說，一個刻度的 ProgressBar 長度變更會對應到一個位元組的安裝。</span><span class="sxs-lookup"><span data-stu-id="57ad8-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="57ad8-117">例如，如果安裝程式在寫入一個登錄機碼時安裝大約10000個位元組，您可以指定遞增中有10000個刻度。</span><span class="sxs-lookup"><span data-stu-id="57ad8-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="57ad8-118">指定或計算自訂動作新增至 [ProgressBar](progressbar-control.md)長度的總刻度數。</span><span class="sxs-lookup"><span data-stu-id="57ad8-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="57ad8-119">自訂動作加入的刻度數目通常會計算為： (刻度遞增) x () 的專案數目。</span><span class="sxs-lookup"><span data-stu-id="57ad8-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="57ad8-120">例如，如果自訂動作寫入10個登錄機碼，安裝程式就會安裝大約100000個位元組，因此安裝程式必須增加 ProgressBar 最後總長度的估計值（依100000刻度）。</span><span class="sxs-lookup"><span data-stu-id="57ad8-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="57ad8-121">若要以動態方式計算，自訂動作必須包含在腳本產生期間立即執行的區段。</span><span class="sxs-lookup"><span data-stu-id="57ad8-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="57ad8-122">延後執行自訂動作所報告的刻度數量必須等於由立即執行動作新增至總滴答計數的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="57ad8-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="57ad8-123">如果不是這種情況，TimeRemaining 文字控制項所報告的剩餘時間將會不正確。</span><span class="sxs-lookup"><span data-stu-id="57ad8-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="57ad8-124">將自訂動作區分為兩個部分的程式碼：在腳本產生階段期間執行的區段，以及在安裝執行階段期間執行的區段。</span><span class="sxs-lookup"><span data-stu-id="57ad8-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="57ad8-125">您可以使用兩個檔案來執行這項作業，也可以透過在安裝程式的執行模式上進行調節來使用一個檔案。</span><span class="sxs-lookup"><span data-stu-id="57ad8-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="57ad8-126">下列範例會使用一個檔案並檢查安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="57ad8-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="57ad8-127">範例的區段會根據安裝程式是否在安裝的執行或腳本產生階段，來執行。</span><span class="sxs-lookup"><span data-stu-id="57ad8-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="57ad8-128">腳本產生期間執行的區段應該會增加 [ProgressBar](progressbar-control.md) 最後總長度的估計值（依自訂動作中的總刻度數）。</span><span class="sxs-lookup"><span data-stu-id="57ad8-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="57ad8-129">這是藉由傳送 **ProgressAddition** 進度訊息來完成。</span><span class="sxs-lookup"><span data-stu-id="57ad8-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="57ad8-130">在安裝執行階段期間執行的區段應該設定郵件內文和範本，以通知使用者自訂動作的作用，以及指示安裝程式更新 [ProgressBar](progressbar-control.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="57ad8-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="57ad8-131">例如，通知安裝程式將 ProgressBar 向前移動一次，並使用每個更新傳送明確的進度訊息。</span><span class="sxs-lookup"><span data-stu-id="57ad8-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="57ad8-132">如果自訂動作正在安裝某個東西，此區段中通常會有一個迴圈。</span><span class="sxs-lookup"><span data-stu-id="57ad8-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="57ad8-133">每次通過此迴圈時，安裝程式都可以安裝一個參考專案，例如登錄機碼，並更新 ProgressBar 控制項</span><span class="sxs-lookup"><span data-stu-id="57ad8-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="57ad8-134">將立即執行自訂動作新增至 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="57ad8-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="57ad8-135">此自訂動作會通知 [ProgressBar](progressbar-control.md) 在安裝的取得和腳本產生階段期間，要進多少。</span><span class="sxs-lookup"><span data-stu-id="57ad8-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="57ad8-136">在下列範例中，來源是藉由編譯範例程式碼所建立的 DLL，而目標則是 CAProgress 的進入點。</span><span class="sxs-lookup"><span data-stu-id="57ad8-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="57ad8-137">將順延強制自訂動作新增至 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="57ad8-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="57ad8-138">此自訂動作會完成實際安裝的步驟，並在安裝程式執行安裝腳本時，通知 [ProgressBar](progressbar-control.md) 有多少可將長條前進。</span><span class="sxs-lookup"><span data-stu-id="57ad8-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="57ad8-139">在下列範例中，來源是藉由編譯範例程式碼所建立的 DLL，而目標則是 CAProgress 的進入點。</span><span class="sxs-lookup"><span data-stu-id="57ad8-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="57ad8-140">在[InstallExecuteSequence](installexecutesequence-table.md)資料表的[InstallInitialize](installinitialize-action.md)和[InstallFinalize](installfinalize-action.md)之間，排程自訂動作。</span><span class="sxs-lookup"><span data-stu-id="57ad8-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="57ad8-141">延遲的自訂動作應該在立即執行自訂動作之後立即排程。</span><span class="sxs-lookup"><span data-stu-id="57ad8-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="57ad8-142">安裝程式在執行腳本之前，不會執行延遲的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="57ad8-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="57ad8-143">下列範例會示範如何將自訂動作新增至 [ProgressBar](progressbar-control.md)。</span><span class="sxs-lookup"><span data-stu-id="57ad8-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="57ad8-144">這兩個自訂動作的來源都是藉由編譯範例程式碼所建立的 DLL，而這兩個自訂動作的目標是 CAProgress 的進入點。</span><span class="sxs-lookup"><span data-stu-id="57ad8-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="57ad8-145">這個範例不會對系統進行任何實際的變更，但會將 ProgressBar 的運作方式，就像是安裝10個以上大約10000個位元組大小的參考專案一樣。</span><span class="sxs-lookup"><span data-stu-id="57ad8-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="57ad8-146">安裝程式會在每次安裝參考專案時更新訊息和 ProgressBar。</span><span class="sxs-lookup"><span data-stu-id="57ad8-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


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



 

 



