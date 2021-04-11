---
description: 使用 MsiProcessMessage 傳送的訊息，與 INSTALLUI 處理常式回呼函數所接收的訊息相同（ \_ 如果呼叫 MsiSetExternalUI）。
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: 使用 MsiProcessMessage 將訊息傳送至 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945321"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="cfae6-103">使用 MsiProcessMessage 將訊息傳送至 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cfae6-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="cfae6-104">使用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 傳送的訊息，與 [**INSTALLUI \_ 處理常式**](/windows/desktop/api/Msi/nc-msi-installui_handlera) 回呼函數所接收的訊息相同（如果呼叫 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) ）。</span><span class="sxs-lookup"><span data-stu-id="cfae6-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="cfae6-105">否則，Windows Installer 會處理訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="cfae6-106">如需詳細資訊，請參閱 [剖析 Windows Installer 的訊息](parsing-windows-installer-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="cfae6-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="cfae6-107">例如，若要傳送 INSTALLMESSAGE \_ 錯誤訊息與 mb \_ ICONWARNING 圖示和 mb \_ ABORTRETRYCANCEL 按鈕：</span><span class="sxs-lookup"><span data-stu-id="cfae6-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="cfae6-108">其中 *hInstall* 是安裝的控制碼，提供給自訂動作或 [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)或 [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)的 *hProduct* 控制碼，而 *hRec* 則是包含要格式化之錯誤資訊的記錄。</span><span class="sxs-lookup"><span data-stu-id="cfae6-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="cfae6-109">如需如何執行格式的詳細資訊，請參閱 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)。</span><span class="sxs-lookup"><span data-stu-id="cfae6-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="cfae6-110">根據預設，如果傳送 INSTALLMESSAGE \_ 錯誤或 INSTALLMESSAGE \_ FATALEXIT 訊息時未指定按鈕類型或圖示類型，則會 \_ 使用 [mb 確定]、[無] 圖示和 [mb \_ DEFBUTTON1]。</span><span class="sxs-lookup"><span data-stu-id="cfae6-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="cfae6-111">Windows Installer 在顯示具有 MB ABORTRETRYIGNORE 按鈕規格的 MessageBox 時，不會將 [ **中止** ] 按鈕標示為「中止」 \_ ，而是會將具有「取消」字串的按鈕加上標籤。</span><span class="sxs-lookup"><span data-stu-id="cfae6-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="cfae6-112">所有錯誤訊息都不會使用 "Abort" 這個字，而是改用 "Cancel" 這個字。</span><span class="sxs-lookup"><span data-stu-id="cfae6-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="cfae6-113">[**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)函數的 *hRecord* 參數取決於傳送至 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)的訊息類型。</span><span class="sxs-lookup"><span data-stu-id="cfae6-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="cfae6-114">下列清單詳細說明記錄相對於訊息類型的需求：</span><span class="sxs-lookup"><span data-stu-id="cfae6-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="cfae6-115">INSTALLMESSAGE \_ FATALEXIT</span><span class="sxs-lookup"><span data-stu-id="cfae6-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="cfae6-116">INSTALLMESSAGE \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="cfae6-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="cfae6-117">INSTALLMESSAGE \_ OUTOFDISKSPACE</span><span class="sxs-lookup"><span data-stu-id="cfae6-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="cfae6-118">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-118">Field</span></span>         | <span data-ttu-id="cfae6-119">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae6-120">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-120">0</span></span>             | <span data-ttu-id="cfae6-121">結果字串格式的範本。</span><span class="sxs-lookup"><span data-stu-id="cfae6-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="cfae6-122">如需詳細資訊，請參閱 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 。</span><span class="sxs-lookup"><span data-stu-id="cfae6-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="cfae6-123">記錄的欄位是使用 \[ 1 \] 代表欄位1、 \[ 2 \] 表示欄位2等等。</span><span class="sxs-lookup"><span data-stu-id="cfae6-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="cfae6-124">1到 *n*</span><span class="sxs-lookup"><span data-stu-id="cfae6-124">1 through *n*</span></span> | <span data-ttu-id="cfae6-125">所有後續的欄位都與欄位0中範本所參考的欄位直接相關。</span><span class="sxs-lookup"><span data-stu-id="cfae6-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="cfae6-126">如果欄位0是 null，則 UI 處理常式收到的字串會格式化為：1： \[ 欄位 1 2 的資料 \] ： \[ 欄位2的資料 \] ，這表示針對記錄的每個欄位，此字串會包含欄位編號，後面接著儲存在欄位中的資料。</span><span class="sxs-lookup"><span data-stu-id="cfae6-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="cfae6-127">當 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)、'/l '[命令列選項](command-line-options.md)或 [記錄原則](logging.md)指定 ' I ' 或 INSTALLLOGMODE 資訊時，會記錄來自 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)的資訊訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cfae6-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="cfae6-128">INSTALLMESSAGE \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="cfae6-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="cfae6-129">INSTALLMESSAGE \_ 警告</span><span class="sxs-lookup"><span data-stu-id="cfae6-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="cfae6-130">INSTALLMESSAGE \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="cfae6-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="cfae6-131">使用錯誤資料表中的訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="cfae6-132">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-132">Field</span></span>         | <span data-ttu-id="cfae6-133">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="cfae6-134">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-134">0</span></span>             | <span data-ttu-id="cfae6-135">必須是 null。</span><span class="sxs-lookup"><span data-stu-id="cfae6-135">Must be null.</span></span>                                         |
| <span data-ttu-id="cfae6-136">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-136">1</span></span>             | <span data-ttu-id="cfae6-137">[錯誤資料表](error-table.md)中的訊息編號。</span><span class="sxs-lookup"><span data-stu-id="cfae6-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="cfae6-138">2到 *n*</span><span class="sxs-lookup"><span data-stu-id="cfae6-138">2 through *n*</span></span> | <span data-ttu-id="cfae6-139">與錯誤資料表中指定的訊息相關。</span><span class="sxs-lookup"><span data-stu-id="cfae6-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="cfae6-140">例如，</span><span class="sxs-lookup"><span data-stu-id="cfae6-140">For example.</span></span>



| <span data-ttu-id="cfae6-141">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-141">Field</span></span> | <span data-ttu-id="cfae6-142">類型</span><span class="sxs-lookup"><span data-stu-id="cfae6-142">Type</span></span>   | <span data-ttu-id="cfae6-143">資料</span><span class="sxs-lookup"><span data-stu-id="cfae6-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="cfae6-144">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-144">0</span></span>     | <span data-ttu-id="cfae6-145">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-145">string</span></span> | <span data-ttu-id="cfae6-146">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-146">null</span></span>       |
| <span data-ttu-id="cfae6-147">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-147">1</span></span>     | <span data-ttu-id="cfae6-148">int</span><span class="sxs-lookup"><span data-stu-id="cfae6-148">int</span></span>    | <span data-ttu-id="cfae6-149">1304</span><span class="sxs-lookup"><span data-stu-id="cfae6-149">1304</span></span>       |
| <span data-ttu-id="cfae6-150">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-150">2</span></span>     | <span data-ttu-id="cfae6-151">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-151">string</span></span> | <span data-ttu-id="cfae6-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="cfae6-152">Myfile.txt</span></span> |



 

<span data-ttu-id="cfae6-153">從 UI 處理常式收到的產生的訊息為：</span><span class="sxs-lookup"><span data-stu-id="cfae6-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="cfae6-154">錯誤1304。</span><span class="sxs-lookup"><span data-stu-id="cfae6-154">Error 1304.</span></span> <span data-ttu-id="cfae6-155">寫入檔案時發生錯誤： Myfile.txt。</span><span class="sxs-lookup"><span data-stu-id="cfae6-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="cfae6-156">確認您有存取該目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="cfae6-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="cfae6-157">如果欄位0不是 null，則會覆寫錯誤資料表中的訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="cfae6-158">相反地，「欄位0」範本會決定訊息的格式。</span><span class="sxs-lookup"><span data-stu-id="cfae6-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="cfae6-159">此訊息也可以指定按鈕（包括預設按鈕），以及與上面所述的訊息搭配使用的圖示。</span><span class="sxs-lookup"><span data-stu-id="cfae6-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="cfae6-160">按鈕和圖示類型會列在 [**INSTALLUI \_ 處理常式**](/windows/desktop/api/Msi/nc-msi-installui_handlera)中。</span><span class="sxs-lookup"><span data-stu-id="cfae6-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="cfae6-161">INSTALLMESSAGE \_ COMMONDATA</span><span class="sxs-lookup"><span data-stu-id="cfae6-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="cfae6-162">傳送此訊息以啟用或停用 [進度] 對話方塊中的 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="cfae6-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="cfae6-163">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-163">Field</span></span> | <span data-ttu-id="cfae6-164">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae6-165">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-165">0</span></span>     | <span data-ttu-id="cfae6-166">未使用的。</span><span class="sxs-lookup"><span data-stu-id="cfae6-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="cfae6-167">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-167">1</span></span>     | <span data-ttu-id="cfae6-168">2指的是 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="cfae6-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="cfae6-169">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-169">2</span></span>     | <span data-ttu-id="cfae6-170">值為1表示應該可以看到 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="cfae6-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="cfae6-171">0值表示 [ **取消** ] 按鈕應該是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="cfae6-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="cfae6-172">例如，若要停用或隱藏 [ **取消** ] 按鈕，記錄會如下所示。</span><span class="sxs-lookup"><span data-stu-id="cfae6-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="cfae6-173">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-173">Field</span></span> | <span data-ttu-id="cfae6-174">類型</span><span class="sxs-lookup"><span data-stu-id="cfae6-174">Type</span></span>   | <span data-ttu-id="cfae6-175">資料</span><span class="sxs-lookup"><span data-stu-id="cfae6-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="cfae6-176">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-176">0</span></span>     | <span data-ttu-id="cfae6-177">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-177">string</span></span> | <span data-ttu-id="cfae6-178">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-178">null</span></span> |
| <span data-ttu-id="cfae6-179">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-179">1</span></span>     | <span data-ttu-id="cfae6-180">int</span><span class="sxs-lookup"><span data-stu-id="cfae6-180">int</span></span>    | <span data-ttu-id="cfae6-181">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-181">2</span></span>    |
| <span data-ttu-id="cfae6-182">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-182">2</span></span>     | <span data-ttu-id="cfae6-183">int</span><span class="sxs-lookup"><span data-stu-id="cfae6-183">int</span></span>    | <span data-ttu-id="cfae6-184">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-184">0</span></span>    |



 

<span data-ttu-id="cfae6-185">INSTALLMESSAGE \_ ACTIONSTART</span><span class="sxs-lookup"><span data-stu-id="cfae6-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="cfae6-186">INSTALLMESSAGE \_ ACTIONDATA</span><span class="sxs-lookup"><span data-stu-id="cfae6-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="cfae6-187">INSTALLMESSAGE \_ ACTIONSTART 記錄會決定 ActionData 記錄的格式。</span><span class="sxs-lookup"><span data-stu-id="cfae6-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="cfae6-188">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-188">Field</span></span> | <span data-ttu-id="cfae6-189">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae6-190">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-190">0</span></span>     | <span data-ttu-id="cfae6-191">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-191">null</span></span>                                                                                                          |
| <span data-ttu-id="cfae6-192">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-192">1</span></span>     | <span data-ttu-id="cfae6-193">動作名稱。</span><span class="sxs-lookup"><span data-stu-id="cfae6-193">Action name.</span></span> <span data-ttu-id="cfae6-194">此欄位中的名稱必須是非 null。</span><span class="sxs-lookup"><span data-stu-id="cfae6-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="cfae6-195">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-195">2</span></span>     | <span data-ttu-id="cfae6-196">動作描述。</span><span class="sxs-lookup"><span data-stu-id="cfae6-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="cfae6-197">3</span><span class="sxs-lookup"><span data-stu-id="cfae6-197">3</span></span>     | <span data-ttu-id="cfae6-198">動作範本。</span><span class="sxs-lookup"><span data-stu-id="cfae6-198">Action template.</span></span> <span data-ttu-id="cfae6-199">這是用於根據此範本格式化訊息的 ActionData。</span><span class="sxs-lookup"><span data-stu-id="cfae6-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="cfae6-200">請勿在動作範本訊息中參考欄位0。</span><span class="sxs-lookup"><span data-stu-id="cfae6-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="cfae6-201">INSTALLMESSAGE \_ ACTIONDATA 記錄的格式如下。</span><span class="sxs-lookup"><span data-stu-id="cfae6-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="cfae6-202">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-202">Field</span></span>         | <span data-ttu-id="cfae6-203">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae6-204">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-204">0</span></span>             | <span data-ttu-id="cfae6-205">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="cfae6-206">1到 *n*</span><span class="sxs-lookup"><span data-stu-id="cfae6-206">1 through *n*</span></span> | <span data-ttu-id="cfae6-207">相依于 \_ [ActionText 資料表](actiontext-table.md)中所指定之對應 INSTALLMESSAGE ACTIONSTART 訊息或範本的欄位3。</span><span class="sxs-lookup"><span data-stu-id="cfae6-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="cfae6-208">例如，INSTALLMESSAGE \_ ACTIONSTART 記錄。</span><span class="sxs-lookup"><span data-stu-id="cfae6-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="cfae6-209">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-209">Field</span></span> | <span data-ttu-id="cfae6-210">類型</span><span class="sxs-lookup"><span data-stu-id="cfae6-210">Type</span></span>   | <span data-ttu-id="cfae6-211">資料</span><span class="sxs-lookup"><span data-stu-id="cfae6-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="cfae6-212">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-212">0</span></span>     | <span data-ttu-id="cfae6-213">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-213">string</span></span> | <span data-ttu-id="cfae6-214">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-214">null</span></span>                                                            |
| <span data-ttu-id="cfae6-215">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-215">1</span></span>     | <span data-ttu-id="cfae6-216">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-216">string</span></span> | <span data-ttu-id="cfae6-217">MyAction</span><span class="sxs-lookup"><span data-stu-id="cfae6-217">MyAction</span></span>                                                        |
| <span data-ttu-id="cfae6-218">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-218">2</span></span>     | <span data-ttu-id="cfae6-219">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-219">string</span></span> | <span data-ttu-id="cfae6-220">這是 "MyAction" 的描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="cfae6-221">3</span><span class="sxs-lookup"><span data-stu-id="cfae6-221">3</span></span>     | <span data-ttu-id="cfae6-222">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-222">string</span></span> | <span data-ttu-id="cfae6-223">MyAction 範本： field1 資料為 \[ 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="cfae6-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="cfae6-224">欄位2資料是 \[ 2 \] 。</span><span class="sxs-lookup"><span data-stu-id="cfae6-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="cfae6-225">INSTALLMESSAGE \_ ACTIONSTART (欄位3的範本) 參考欄位1和2，INSTALLMESSAGE \_ ACTIONDATA 記錄應該有2個欄位包含所保證的資料。</span><span class="sxs-lookup"><span data-stu-id="cfae6-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="cfae6-226">這些欄位可以是 [字串] 或 [整數] 欄位。</span><span class="sxs-lookup"><span data-stu-id="cfae6-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="cfae6-227">INSTALLMESSAGE \_ ACTIONDATA 記錄。</span><span class="sxs-lookup"><span data-stu-id="cfae6-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="cfae6-228">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-228">Field</span></span> | <span data-ttu-id="cfae6-229">類型</span><span class="sxs-lookup"><span data-stu-id="cfae6-229">Type</span></span>   | <span data-ttu-id="cfae6-230">資料</span><span class="sxs-lookup"><span data-stu-id="cfae6-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="cfae6-231">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-231">0</span></span>     | <span data-ttu-id="cfae6-232">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-232">string</span></span> | <span data-ttu-id="cfae6-233">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-233">null</span></span>                    |
| <span data-ttu-id="cfae6-234">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-234">1</span></span>     | <span data-ttu-id="cfae6-235">int</span><span class="sxs-lookup"><span data-stu-id="cfae6-235">int</span></span>    | <span data-ttu-id="cfae6-236">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-236">2</span></span>                       |
| <span data-ttu-id="cfae6-237">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-237">2</span></span>     | <span data-ttu-id="cfae6-238">字串</span><span class="sxs-lookup"><span data-stu-id="cfae6-238">string</span></span> | <span data-ttu-id="cfae6-239">適用于 MyAction 的 ActionData</span><span class="sxs-lookup"><span data-stu-id="cfae6-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="cfae6-240">INSTALLMESSAGE \_ FILESINUSE</span><span class="sxs-lookup"><span data-stu-id="cfae6-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="cfae6-241">FILESINUSE 記錄是可變長度的記錄。</span><span class="sxs-lookup"><span data-stu-id="cfae6-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="cfae6-242">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-242">Field</span></span> | <span data-ttu-id="cfae6-243">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae6-244">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-244">0</span></span>     | <span data-ttu-id="cfae6-245">這個欄位可以是 null。</span><span class="sxs-lookup"><span data-stu-id="cfae6-245">This field can be null.</span></span> <span data-ttu-id="cfae6-246">針對使用基本 UI 的安裝，此欄位可能會指定靜態文字，以在 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)的[ListBox 控制項](listbox-control.md)中顯示。</span><span class="sxs-lookup"><span data-stu-id="cfae6-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="cfae6-247">針對使用完整 UI 的安裝，此欄位不會有任何作用，因為文字是由撰寫自訂 FilesInUse 對話方塊所指定。</span><span class="sxs-lookup"><span data-stu-id="cfae6-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="cfae6-248">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-248">1</span></span>     | <span data-ttu-id="cfae6-249">使用中的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cfae6-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cfae6-250">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-250">2</span></span>     | <span data-ttu-id="cfae6-251">此欄位會識別保留使用中檔案的進程。**Windows Installer 版本4.0：** 進程的處理序識別碼 (PID) ，或進程的視窗標題。</span><span class="sxs-lookup"><span data-stu-id="cfae6-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="cfae6-252">**Windows Installer 3.1 版及更早版本：** 此欄位必須是進程的處理序識別碼 (PID) 。</span><span class="sxs-lookup"><span data-stu-id="cfae6-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="cfae6-253">例如，若要傳送 FilesInUse 訊息以顯示使用中的兩個檔案，red.exe 和 blue.exe，記錄有四個欄位加上0欄位。</span><span class="sxs-lookup"><span data-stu-id="cfae6-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="cfae6-254">記錄格式如下表所示。</span><span class="sxs-lookup"><span data-stu-id="cfae6-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="cfae6-255">此範例需要 Windows Installer 4.0 版。</span><span class="sxs-lookup"><span data-stu-id="cfae6-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="cfae6-256">**Windows Installer 3.1 版及更早版本：** 下列範例中的欄位2和4必須包含持有 red.exe 之進程的 Pid，以及使用 blue.exe。</span><span class="sxs-lookup"><span data-stu-id="cfae6-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="cfae6-257">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-257">Field</span></span> | <span data-ttu-id="cfae6-258">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="cfae6-259">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-259">0</span></span>     | <span data-ttu-id="cfae6-260">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-260">null</span></span>              |
| <span data-ttu-id="cfae6-261">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-261">1</span></span>     | <span data-ttu-id="cfae6-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="cfae6-262">Red.exe</span></span>           |
| <span data-ttu-id="cfae6-263">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-263">2</span></span>     | <span data-ttu-id="cfae6-264">紅色視窗標題</span><span class="sxs-lookup"><span data-stu-id="cfae6-264">Red Window Title</span></span>  |
| <span data-ttu-id="cfae6-265">3</span><span class="sxs-lookup"><span data-stu-id="cfae6-265">3</span></span>     | <span data-ttu-id="cfae6-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="cfae6-266">Blue.exe</span></span>          |
| <span data-ttu-id="cfae6-267">4</span><span class="sxs-lookup"><span data-stu-id="cfae6-267">4</span></span>     | <span data-ttu-id="cfae6-268">藍色視窗標題</span><span class="sxs-lookup"><span data-stu-id="cfae6-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="cfae6-269">在 Windows Installer 4.0 版中，如果從服務傳遞的 PID 沒有視窗標題（例如系統匣應用程式），則不會顯示該檔案，而且詳細資訊記錄檔會包含下列訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="cfae6-270">INSTALLMESSAGE \_ RESOLVESOURCE</span><span class="sxs-lookup"><span data-stu-id="cfae6-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="cfae6-271">INSTALLMESSAGE \_ RESOLVESOURCE 記錄有七個欄位。</span><span class="sxs-lookup"><span data-stu-id="cfae6-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="cfae6-272">為了讓 INSTALLMESSAGE \_ RESOLVESOURCE 能夠正常運作，外部 UI 處理常式可能不會處理 INSTALLMESSAGE \_ RESOLVESOURCE 訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="cfae6-273">Windows Installer 必須處理 INSTALLMESSAGE \_ RESOLVESOURCE 訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="cfae6-274">也就是說，在篩選 INSTALLMESSAGE RESOLVESOURCE 訊息時，外部 UI 處理常式會傳回0，表示「不採取任何動作」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cfae6-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="cfae6-275">最佳做法是避免傳送 RESOLVESOURCE 的訊息。</span><span class="sxs-lookup"><span data-stu-id="cfae6-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="cfae6-276">欄位</span><span class="sxs-lookup"><span data-stu-id="cfae6-276">Field</span></span> | <span data-ttu-id="cfae6-277">描述</span><span class="sxs-lookup"><span data-stu-id="cfae6-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae6-278">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-278">0</span></span>     | <span data-ttu-id="cfae6-279">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="cfae6-280">1</span><span class="sxs-lookup"><span data-stu-id="cfae6-280">1</span></span>     | <span data-ttu-id="cfae6-281">null</span><span class="sxs-lookup"><span data-stu-id="cfae6-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="cfae6-282">2</span><span class="sxs-lookup"><span data-stu-id="cfae6-282">2</span></span>     | <span data-ttu-id="cfae6-283">封裝名稱。</span><span class="sxs-lookup"><span data-stu-id="cfae6-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="cfae6-284">3</span><span class="sxs-lookup"><span data-stu-id="cfae6-284">3</span></span>     | <span data-ttu-id="cfae6-285">產品代碼。</span><span class="sxs-lookup"><span data-stu-id="cfae6-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="cfae6-286">4</span><span class="sxs-lookup"><span data-stu-id="cfae6-286">4</span></span>     | <span data-ttu-id="cfae6-287">相對路徑（如果已知）可以是 null。</span><span class="sxs-lookup"><span data-stu-id="cfae6-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="cfae6-288">5</span><span class="sxs-lookup"><span data-stu-id="cfae6-288">5</span></span>     | <span data-ttu-id="cfae6-289">0</span><span class="sxs-lookup"><span data-stu-id="cfae6-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="cfae6-290">6</span><span class="sxs-lookup"><span data-stu-id="cfae6-290">6</span></span>     | <span data-ttu-id="cfae6-291">是否要驗證封裝程式碼。</span><span class="sxs-lookup"><span data-stu-id="cfae6-291">Whether to validate the package code.</span></span> <span data-ttu-id="cfae6-292">值為 ' 1 ' 表示應驗證封裝程式碼。</span><span class="sxs-lookup"><span data-stu-id="cfae6-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="cfae6-293">值為 ' 0 ' 表示不應驗證套件。</span><span class="sxs-lookup"><span data-stu-id="cfae6-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="cfae6-294">7</span><span class="sxs-lookup"><span data-stu-id="cfae6-294">7</span></span>     | <span data-ttu-id="cfae6-295">媒體資料表中所需的磁片。</span><span class="sxs-lookup"><span data-stu-id="cfae6-295">Required disk from media table.</span></span> <span data-ttu-id="cfae6-296">值為 ' 0 ' 表示可接受任何磁片。</span><span class="sxs-lookup"><span data-stu-id="cfae6-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




