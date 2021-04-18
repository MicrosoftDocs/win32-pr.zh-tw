---
description: 外部 UI 處理常式可以處理 MsiSetExternalUI 函數的 dwMessagedFilter 參數所指定的安裝程式訊息清單。
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: 剖析 Windows Installer 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192104"
---
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="69e25-103">剖析 Windows Installer 訊息</span><span class="sxs-lookup"><span data-stu-id="69e25-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="69e25-104">外部 UI 處理常式可以處理 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)函數的 *dwMessagedFilter* 參數所指定的安裝程式訊息清單。</span><span class="sxs-lookup"><span data-stu-id="69e25-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="69e25-105">其中有些訊息包含可直接使用的字串，而外部 UI 處理常式可能需要剖析和處理其他訊息才能發揮效用。</span><span class="sxs-lookup"><span data-stu-id="69e25-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="69e25-106">您的外部 UI 處理常式可能只需要監視 Windows Installer 的訊息，而不需要執行任何會影響安裝的操作。</span><span class="sxs-lookup"><span data-stu-id="69e25-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="69e25-107">下列 Windows Installer 訊息包含可由對話方塊顯示，且不需要額外處理的字串。</span><span class="sxs-lookup"><span data-stu-id="69e25-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="69e25-108">這些訊息包含要由對話方塊顯示的按鈕和圖示清單。</span><span class="sxs-lookup"><span data-stu-id="69e25-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="69e25-109">您可以使用 **mb \_ ICONMASK**、 **mb \_ DEFMASK** 和 **mb \_ TYPEMASK** 值來指定圖示和按鈕。</span><span class="sxs-lookup"><span data-stu-id="69e25-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="69e25-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**</span><span class="sxs-lookup"><span data-stu-id="69e25-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-111">發生過早終止的安裝。</span><span class="sxs-lookup"><span data-stu-id="69e25-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="69e25-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-113">格式化錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE \_ 警告**</span><span class="sxs-lookup"><span data-stu-id="69e25-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-115">格式化的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="69e25-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-117">格式化的記錄訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="69e25-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-119">格式化的使用者訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**</span><span class="sxs-lookup"><span data-stu-id="69e25-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-121">指出磁碟空間不足狀況的格式化訊息</span><span class="sxs-lookup"><span data-stu-id="69e25-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="69e25-122">外部使用者處理常式可以使用下列 Windows Installer 訊息來監視 Windows Installer UI 的順序。</span><span class="sxs-lookup"><span data-stu-id="69e25-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="69e25-123">安裝程式會在 Windows Installer UI 序列的開頭傳送這些訊息，因為每個對話方塊都會顯示在 UI 順序的結尾。</span><span class="sxs-lookup"><span data-stu-id="69e25-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="69e25-124">使用這些訊息不需要處理。</span><span class="sxs-lookup"><span data-stu-id="69e25-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="69e25-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE \_ 終止</span><span class="sxs-lookup"><span data-stu-id="69e25-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="69e25-126">此訊息表示 UI 順序的結尾。</span><span class="sxs-lookup"><span data-stu-id="69e25-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="69e25-127">字串為 null 字串。</span><span class="sxs-lookup"><span data-stu-id="69e25-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE \_ INITIALIZE</span><span class="sxs-lookup"><span data-stu-id="69e25-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="69e25-129">此訊息表示 UI 序列已啟動。</span><span class="sxs-lookup"><span data-stu-id="69e25-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="69e25-130">字串為 null 字串。</span><span class="sxs-lookup"><span data-stu-id="69e25-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG</span><span class="sxs-lookup"><span data-stu-id="69e25-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="69e25-132">字串包含目前對話方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="69e25-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="69e25-133">下列 Windows Installer 訊息需要外部 UI 處理常式進行額外的處理。</span><span class="sxs-lookup"><span data-stu-id="69e25-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="69e25-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ RESOLVESOURCE**</span><span class="sxs-lookup"><span data-stu-id="69e25-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-135">外部使用者介面處理常式必須傳回0，並允許 Windows Installer 處理訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="69e25-136">外部使用者介面處理常式可以監視這則訊息，但不應該執行任何影響安裝的動作。</span><span class="sxs-lookup"><span data-stu-id="69e25-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="69e25-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="69e25-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-138">外部 UI 應該會顯示 [FilesInUse 對話方塊](filesinuse-dialog.md) ，以回應這則訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="69e25-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-140">外部 UI 應該會顯示 [MsiRMFilesInUse 對話方塊](msirmfilesinuse-dialog.md) ，以回應這則訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="69e25-141">從 Windows Installer 4.0 版開始提供。</span><span class="sxs-lookup"><span data-stu-id="69e25-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="69e25-142">如需此訊息的詳細資訊，請參閱搭配 [外部 UI 使用重新開機管理員](using-restart-manager-with-an-external-ui-.md)。</span><span class="sxs-lookup"><span data-stu-id="69e25-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="69e25-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**</span><span class="sxs-lookup"><span data-stu-id="69e25-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-144">這則訊息會提供有關目前動作的資訊。</span><span class="sxs-lookup"><span data-stu-id="69e25-144">This message gives information about the current action.</span></span> <span data-ttu-id="69e25-145">格式為 Action \[ 1 \] ： \[ 2 \] 。</span><span class="sxs-lookup"><span data-stu-id="69e25-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="69e25-146">\[3 \] ，其中冒號會用來分隔欄位1和欄位2，而句號用來分隔欄位2和欄位3。</span><span class="sxs-lookup"><span data-stu-id="69e25-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="69e25-147">[欄位 \[ 1] \] 包含使用 [**時間**](time.md) 屬性格式啟動動作的時間。</span><span class="sxs-lookup"><span data-stu-id="69e25-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="69e25-148">欄位 \[ 2 \] 包含順序資料表中的動作名稱。</span><span class="sxs-lookup"><span data-stu-id="69e25-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="69e25-149">欄位 \[ 3 \] 提供來自 [ActionText 資料表](actiontext-table.md) 或 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 函數的動作描述。</span><span class="sxs-lookup"><span data-stu-id="69e25-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**</span><span class="sxs-lookup"><span data-stu-id="69e25-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-151">這個字串的格式是由 [ActionText 資料表](actiontext-table.md)或 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)函數所提供的 [範本](template.md)值所指定。</span><span class="sxs-lookup"><span data-stu-id="69e25-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="69e25-152">**INSTALLMESSAGE \_ ACTIONSTART** 訊息之後可能會有無限數量的 **INSTALLMESSAGE \_ ACTIONDATA** 訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**</span><span class="sxs-lookup"><span data-stu-id="69e25-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="69e25-154">此訊息有三個子類型： Language、Caption 和 CancelShow。</span><span class="sxs-lookup"><span data-stu-id="69e25-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="69e25-155">字串可以有三個欄位，並以數位分隔，後面接著冒號。</span><span class="sxs-lookup"><span data-stu-id="69e25-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="69e25-156">並非所有欄位都是必要欄位。</span><span class="sxs-lookup"><span data-stu-id="69e25-156">Not all fields are required.</span></span> <span data-ttu-id="69e25-157">訊息可以是 Null 或空的 ( "" ) 字串。</span><span class="sxs-lookup"><span data-stu-id="69e25-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="69e25-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言</span><span class="sxs-lookup"><span data-stu-id="69e25-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="69e25-159">[欄位 1] 包含0值，表示此字串包含語言資訊。</span><span class="sxs-lookup"><span data-stu-id="69e25-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="69e25-160">欄位2包含的 [語言](language.md) 值是數位語言識別項 (LANGID。 ) 欄位3是代表 ANSI 字碼頁的值。</span><span class="sxs-lookup"><span data-stu-id="69e25-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>標題</span><span class="sxs-lookup"><span data-stu-id="69e25-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="69e25-162">[欄位 1] 包含值1，表示此字串包含標題或標題的文字。</span><span class="sxs-lookup"><span data-stu-id="69e25-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="69e25-163">欄位2包含外部 UI 處理常式可以用來做為對話方塊標題標題的文字。</span><span class="sxs-lookup"><span data-stu-id="69e25-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="69e25-164">欄位3為 Null 或空白 ( "" ) 字串。</span><span class="sxs-lookup"><span data-stu-id="69e25-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="69e25-165">標題訊息中可能沒有欄位3。</span><span class="sxs-lookup"><span data-stu-id="69e25-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span><span class="sxs-lookup"><span data-stu-id="69e25-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="69e25-167">[欄位 1] 包含值2，表示此字串包含是否顯示 [取消] 按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="69e25-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="69e25-168">如果應該隱藏 [取消] 按鈕，則欄位2會包含0這個值。</span><span class="sxs-lookup"><span data-stu-id="69e25-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="69e25-169">如果應該可以看到 [取消] 按鈕，則欄位2會包含值1。</span><span class="sxs-lookup"><span data-stu-id="69e25-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="69e25-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE \_ 進度</span><span class="sxs-lookup"><span data-stu-id="69e25-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="69e25-171">此訊息有四個子類型： Reset、ActionInfo、ProgressReport 和 ProgressAddition。</span><span class="sxs-lookup"><span data-stu-id="69e25-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="69e25-172">在收到第一個重設進度訊息之前，外部處理常式不應該對這些訊息採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="69e25-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="69e25-173">這會提供進度列的總刻度數的估計值。</span><span class="sxs-lookup"><span data-stu-id="69e25-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="69e25-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>重 置</span><span class="sxs-lookup"><span data-stu-id="69e25-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="69e25-175">[欄位 1] 包含值0，表示重設進度列。</span><span class="sxs-lookup"><span data-stu-id="69e25-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="69e25-176">欄位2包含進度列中的總刻度數。</span><span class="sxs-lookup"><span data-stu-id="69e25-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="69e25-177">欄位3包含向前進度列動作的0值。</span><span class="sxs-lookup"><span data-stu-id="69e25-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="69e25-178">[欄位 3] 包含後置進度列動作的值1。</span><span class="sxs-lookup"><span data-stu-id="69e25-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="69e25-179">欄位4中的值0表示安裝正在進行中，而且可能會計算剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="69e25-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="69e25-180">欄位4中的值1表示正在執行腳本，而「請稍候 ...」可以顯示訊息。</span><span class="sxs-lookup"><span data-stu-id="69e25-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="69e25-181">總刻度數的估計值是近似值，可能不正確。</span><span class="sxs-lookup"><span data-stu-id="69e25-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span><span class="sxs-lookup"><span data-stu-id="69e25-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="69e25-183">[欄位 1] 包含值1，表示此字串包含動作資訊。</span><span class="sxs-lookup"><span data-stu-id="69e25-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="69e25-184">[欄位 2] 包含目前動作所傳送之每個 ActionData 訊息的進度列所移動的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="69e25-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="69e25-185">如果欄位3包含0值，請忽略欄位2。</span><span class="sxs-lookup"><span data-stu-id="69e25-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="69e25-186">如果欄位3包含值1，則依據目前動作所傳送之每個 ActionData 訊息的欄位2中的刻度數目遞增進度列。</span><span class="sxs-lookup"><span data-stu-id="69e25-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="69e25-187">未使用欄位4。</span><span class="sxs-lookup"><span data-stu-id="69e25-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span><span class="sxs-lookup"><span data-stu-id="69e25-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="69e25-189">[欄位 1] 包含值2，表示此字串包含進度資訊。</span><span class="sxs-lookup"><span data-stu-id="69e25-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="69e25-190">欄位2包含進度列移動的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="69e25-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="69e25-191">未使用欄位3。</span><span class="sxs-lookup"><span data-stu-id="69e25-191">Field 3 is unused.</span></span> <span data-ttu-id="69e25-192">未使用欄位4。</span><span class="sxs-lookup"><span data-stu-id="69e25-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="69e25-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="69e25-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="69e25-194">[欄位 1] 包含值3，表示動作可以加入進度列的刻度。</span><span class="sxs-lookup"><span data-stu-id="69e25-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="69e25-195">欄位2包含要加入至總進度刻度的總預期計數的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="69e25-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="69e25-196">未使用欄位3。</span><span class="sxs-lookup"><span data-stu-id="69e25-196">Field 3 is unused.</span></span> <span data-ttu-id="69e25-197">未使用欄位4。</span><span class="sxs-lookup"><span data-stu-id="69e25-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



