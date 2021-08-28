---
description: 外部 UI 處理常式可以處理 MsiSetExternalUI 函數的 dwMessagedFilter 參數所指定的安裝程式訊息清單。
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: 剖析 Windows Installer 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d2d44f75ccd610dd5d4da24a9ad96d85af947474ed1c8e600183388264bbb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942731"
---
# <a name="parsing-windows-installer-messages"></a>剖析 Windows Installer 訊息

外部 UI 處理常式可以處理 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)函數的 *dwMessagedFilter* 參數所指定的安裝程式訊息清單。 其中有些訊息包含可直接使用的字串，而外部 UI 處理常式可能需要剖析和處理其他訊息才能發揮效用。 您的外部 UI 處理常式可能只需要監視 Windows Installer 的訊息，而不需要執行任何會影響安裝的操作。

下列 Windows Installer 訊息包含可由對話方塊顯示，且不需要額外處理的字串。 這些訊息包含要由對話方塊顯示的按鈕和圖示清單。 您可以使用 **mb \_ ICONMASK**、 **mb \_ DEFMASK** 和 **mb \_ TYPEMASK** 值來指定圖示和按鈕。

<dl> <dt>

<span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**
</dt> <dd>

發生過早終止的安裝。

</dd> <dt>

<span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE \_ 錯誤**
</dt> <dd>

格式化錯誤訊息。

</dd> <dt>

<span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE \_ 警告**
</dt> <dd>

格式化的警告訊息。

</dd> <dt>

<span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE \_ 資訊**
</dt> <dd>

格式化的記錄訊息。

</dd> <dt>

<span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE \_ 使用者**
</dt> <dd>

格式化的使用者訊息。

</dd> <dt>

<span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**
</dt> <dd>

指出磁碟空間不足狀況的格式化訊息

</dd> </dl>

外部使用者處理常式可以使用下列 Windows Installer 訊息來監視 Windows Installer UI 的順序。 安裝程式會在 Windows Installer UI 序列的開頭傳送這些訊息，因為每個對話方塊都會顯示在 ui 順序的結尾。 使用這些訊息不需要處理。

<dl> <dt>

<span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE \_ 終止
</dt> <dd>

此訊息表示 UI 順序的結尾。 字串為 null 字串。

</dd> <dt>

<span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE \_ INITIALIZE
</dt> <dd>

此訊息表示 UI 序列已啟動。 字串為 null 字串。

</dd> <dt>

<span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG
</dt> <dd>

字串包含目前對話方塊的名稱。

</dd> </dl>

下列 Windows Installer 訊息需要外部 UI 處理常式進行額外的處理。

<dl> <dt>

<span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ RESOLVESOURCE**
</dt> <dd>

外部使用者介面處理常式必須傳回0，並允許 Windows Installer 處理訊息。 外部使用者介面處理常式可以監視這則訊息，但不應該執行任何影響安裝的動作。

</dd> <dt>

<span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**
</dt> <dd>

外部 UI 應該會顯示 [FilesInUse 對話方塊](filesinuse-dialog.md) ，以回應這則訊息。

</dd> <dt>

<span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**
</dt> <dd>

外部 UI 應該會顯示 [MsiRMFilesInUse 對話方塊](msirmfilesinuse-dialog.md) ，以回應這則訊息。 從 Windows Installer 4.0 版開始提供。 如需此訊息的詳細資訊，請參閱搭配 [外部 UI 使用重新開機管理員](using-restart-manager-with-an-external-ui-.md)。

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**
</dt> <dd>

這則訊息會提供有關目前動作的資訊。 格式為 Action \[ 1 \] ： \[ 2 \] 。 \[3 \] ，其中冒號會用來分隔欄位1和欄位2，而句號用來分隔欄位2和欄位3。 [欄位 \[ 1] \] 包含使用 [**時間**](time.md) 屬性格式啟動動作的時間。 欄位 \[ 2 \] 包含順序資料表中的動作名稱。 欄位 \[ 3 \] 提供來自 [ActionText 資料表](actiontext-table.md) 或 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 函數的動作描述。

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**
</dt> <dd>

這個字串的格式是由 [ActionText 資料表](actiontext-table.md)或 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)函數所提供的 [範本](template.md)值所指定。 **INSTALLMESSAGE \_ ACTIONSTART** 訊息之後可能會有無限數量的 **INSTALLMESSAGE \_ ACTIONDATA** 訊息。

</dd> <dt>

<span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**
</dt> <dd>

此訊息有三個子類型： Language、Caption 和 CancelShow。 字串可以有三個欄位，並以數位分隔，後面接著冒號。 並非所有欄位都是必要欄位。 訊息可以是 Null 或空的 ( "" ) 字串。

<dl> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言
</dt> <dd>

[欄位 1] 包含0值，表示此字串包含語言資訊。 欄位2包含的 [語言](language.md) 值是數位語言識別項 (LANGID。 ) 欄位3是代表 ANSI 字碼頁的值。

</dd> <dt>

<span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>標題
</dt> <dd>

[欄位 1] 包含值1，表示此字串包含標題或標題的文字。 欄位2包含外部 UI 處理常式可以用來做為對話方塊標題標題的文字。 欄位3為 Null 或空白 ( "" ) 字串。 標題訊息中可能沒有欄位3。

</dd> <dt>

<span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow
</dt> <dd>

[欄位 1] 包含值2，表示此字串包含是否顯示 [取消] 按鈕的相關資訊。 如果應該隱藏 [取消] 按鈕，則欄位2會包含0這個值。 如果應該可以看到 [取消] 按鈕，則欄位2會包含值1。

</dd> </dl> </dd> <dt>

<span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE \_ 進度
</dt> <dd>

此訊息有四個子類型： Reset、ActionInfo、ProgressReport 和 ProgressAddition。 在收到第一個重設進度訊息之前，外部處理常式不應該對這些訊息採取任何動作。 這會提供進度列的總刻度數的估計值。

<dl> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>重 置
</dt> <dd>

[欄位 1] 包含值0，表示重設進度列。 欄位2包含進度列中的總刻度數。 欄位3包含向前進度列動作的0值。 [欄位 3] 包含後置進度列動作的值1。 欄位4中的值0表示安裝正在進行中，而且可能會計算剩餘的時間。 欄位4中的值1表示正在執行腳本，而「請稍候 ...」可以顯示訊息。 總刻度數的估計值是近似值，可能不正確。

</dd> <dt>

<span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo
</dt> <dd>

[欄位 1] 包含值1，表示此字串包含動作資訊。 [欄位 2] 包含目前動作所傳送之每個 ActionData 訊息的進度列所移動的刻度數目。 如果欄位3包含0值，請忽略欄位2。 如果欄位3包含值1，則依據目前動作所傳送之每個 ActionData 訊息的欄位2中的刻度數目遞增進度列。 未使用欄位4。

</dd> <dt>

<span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport
</dt> <dd>

[欄位 1] 包含值2，表示此字串包含進度資訊。 欄位2包含進度列移動的刻度數目。 未使用欄位3。 未使用欄位4。

</dd> <dt>

<span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition
</dt> <dd>

[欄位 1] 包含值3，表示動作可以加入進度列的刻度。 欄位2包含要加入至總進度刻度的總預期計數的刻度數目。 未使用欄位3。 未使用欄位4。

</dd> </dl> </dd> </dl>

 

 



