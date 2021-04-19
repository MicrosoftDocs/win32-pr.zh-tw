---
description: WMI 命令列 (WMIC) 公用程式提供適用于 WMI 的命令列介面。
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222926"
---
# <a name="wmic"></a><span data-ttu-id="959d4-103">wmic</span><span class="sxs-lookup"><span data-stu-id="959d4-103">wmic</span></span>

<span data-ttu-id="959d4-104">WMI 命令列 (WMIC) 公用程式提供命令列介面，Windows Management Instrumentation (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="959d4-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="959d4-105">WMIC 與現有的 shell 和公用程式命令相容。</span><span class="sxs-lookup"><span data-stu-id="959d4-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="959d4-106">以下是適用于 WMIC 的一般參考主題。</span><span class="sxs-lookup"><span data-stu-id="959d4-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="959d4-107">如需有關如何使用 WMIC 的詳細資訊和指導方針，包括別名、動詞、交換器和命令的其他資訊，請參閱 [使用 Windows Management Instrumentation 命令列](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) 和 [WMIC-透過 WMI 進行命令列控制](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="959d4-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="959d4-108">Alias</span><span class="sxs-lookup"><span data-stu-id="959d4-108">Alias</span></span>

<span data-ttu-id="959d4-109">別名是類別、屬性或方法的易記重新命名，可讓 WMI 更容易使用和讀取。</span><span class="sxs-lookup"><span data-stu-id="959d4-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="959d4-110">您可以透過/，判斷哪些別名可用於 WMIC **？**</span><span class="sxs-lookup"><span data-stu-id="959d4-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="959d4-111">。</span><span class="sxs-lookup"><span data-stu-id="959d4-111">command.</span></span> <span data-ttu-id="959d4-112">您也可以使用 **<className> /？** 來決定特定類別的別名。</span><span class="sxs-lookup"><span data-stu-id="959d4-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="959d4-113">。</span><span class="sxs-lookup"><span data-stu-id="959d4-113">command.</span></span> <span data-ttu-id="959d4-114">如需詳細資訊，請參閱 [WMIC 別名](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="959d4-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="959d4-115">參數</span><span class="sxs-lookup"><span data-stu-id="959d4-115">Switch</span></span>

<span data-ttu-id="959d4-116">交換器是您可以全域設定或選擇性設定的 WMIC 選項。</span><span class="sxs-lookup"><span data-stu-id="959d4-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="959d4-117">如需可用參數的清單，請參閱 [WMIC 參數](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="959d4-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="959d4-118">動詞</span><span class="sxs-lookup"><span data-stu-id="959d4-118">Verbs</span></span>

<span data-ttu-id="959d4-119">若要在 WMIC 中使用動詞，請輸入別名名稱，後面接著動詞。</span><span class="sxs-lookup"><span data-stu-id="959d4-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="959d4-120">如果別名不支援動詞，您會收到訊息「提供者不能進行嘗試的作業。」</span><span class="sxs-lookup"><span data-stu-id="959d4-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="959d4-121">如需詳細資訊，請參閱 [WMIC 動詞](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="959d4-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="959d4-122">大部分的別名都支援下列動詞。</span><span class="sxs-lookup"><span data-stu-id="959d4-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="959d4-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span><span class="sxs-lookup"><span data-stu-id="959d4-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="959d4-124">`Associators of (<wmi_object>)`傳回查詢的結果，其中 *<wmi \_ 物件>* 是 **path** 或 **CLASS** 命令所傳回之物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="959d4-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="959d4-125">結果是與物件相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="959d4-125">The results are instances associated with the object.</span></span> <span data-ttu-id="959d4-126">當 ASSOC 搭配別名使用時，會傳回具有該別名之類別的類別。</span><span class="sxs-lookup"><span data-stu-id="959d4-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="959d4-127">依預設，輸出會以 HTML 格式傳回。</span><span class="sxs-lookup"><span data-stu-id="959d4-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="959d4-128">ASSOC 動詞有下列參數。</span><span class="sxs-lookup"><span data-stu-id="959d4-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="959d4-129">Switch</span><span class="sxs-lookup"><span data-stu-id="959d4-129">Switch</span></span>                         | <span data-ttu-id="959d4-130">描述</span><span class="sxs-lookup"><span data-stu-id="959d4-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959d4-131">/RESULTCLASS:<classname></span><span class="sxs-lookup"><span data-stu-id="959d4-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="959d4-132">與來源物件相關聯的傳回端點必須屬於或衍生自指定的類別。</span><span class="sxs-lookup"><span data-stu-id="959d4-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="959d4-133">/RESULTROLE:<rolename></span><span class="sxs-lookup"><span data-stu-id="959d4-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="959d4-134">傳回的端點必須在與來源物件的關聯中播放特定的角色。</span><span class="sxs-lookup"><span data-stu-id="959d4-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="959d4-135">/ASSOCCLASS:<assocclass></span><span class="sxs-lookup"><span data-stu-id="959d4-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="959d4-136">傳回的端點必須透過指定的類別或其中一個衍生類別，與來源建立關聯。</span><span class="sxs-lookup"><span data-stu-id="959d4-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="959d4-137">範例： **作業系統 ASSOC**</span><span class="sxs-lookup"><span data-stu-id="959d4-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-138"><span id="CALL"></span><span id="call"></span>叫</span><span class="sxs-lookup"><span data-stu-id="959d4-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="959d4-139">執行方法。</span><span class="sxs-lookup"><span data-stu-id="959d4-139">Executes a method.</span></span>

<span data-ttu-id="959d4-140">範例： **服務的標題 = ' TELNET ' 呼叫 STARTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="959d4-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="959d4-141">若要判斷指定類別的可用方法，請使用 **/？**。</span><span class="sxs-lookup"><span data-stu-id="959d4-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="959d4-142">例如， **服務的標題 = ' TELNET ' CALL/？**</span><span class="sxs-lookup"><span data-stu-id="959d4-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="959d4-143">列出服務類別的可用功能。</span><span class="sxs-lookup"><span data-stu-id="959d4-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="959d4-144"><span id="CREATE"></span><span id="create"></span>創建</span><span class="sxs-lookup"><span data-stu-id="959d4-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-145">建立新的實例，並設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="959d4-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="959d4-146">CREATE 不能用來建立新的類別。</span><span class="sxs-lookup"><span data-stu-id="959d4-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="959d4-147">範例： **環境 CREATE NAME = "TEMP";VARIABLEVALUE = "NEW"**</span><span class="sxs-lookup"><span data-stu-id="959d4-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-148"><span id="DELETE"></span><span id="delete"></span>刪除</span><span class="sxs-lookup"><span data-stu-id="959d4-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-149">刪除目前的實例或實例的集合。</span><span class="sxs-lookup"><span data-stu-id="959d4-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="959d4-150">DELETE 可以用來刪除類別。</span><span class="sxs-lookup"><span data-stu-id="959d4-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="959d4-151">範例： **NAME = "CALC.EXE" DELETE 的進程**</span><span class="sxs-lookup"><span data-stu-id="959d4-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-152"><span id="GET"></span><span id="get"></span>獲取</span><span class="sxs-lookup"><span data-stu-id="959d4-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="959d4-153">取出特定屬性值。</span><span class="sxs-lookup"><span data-stu-id="959d4-153">Retrieve specific property values.</span></span>

<span data-ttu-id="959d4-154">GET 具有下列參數。</span><span class="sxs-lookup"><span data-stu-id="959d4-154">GET has the following switches.</span></span>



| <span data-ttu-id="959d4-155">Switch</span><span class="sxs-lookup"><span data-stu-id="959d4-155">Switch</span></span>                               | <span data-ttu-id="959d4-156">描述</span><span class="sxs-lookup"><span data-stu-id="959d4-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959d4-157">/VALUE</span><span class="sxs-lookup"><span data-stu-id="959d4-157">/VALUE</span></span>                               | <span data-ttu-id="959d4-158">輸出會以個別行上所列出的每個值和屬性的名稱來格式化。</span><span class="sxs-lookup"><span data-stu-id="959d4-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="959d4-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="959d4-159">/ALL</span></span>                                 | <span data-ttu-id="959d4-160">輸出會格式化為表格。</span><span class="sxs-lookup"><span data-stu-id="959d4-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="959d4-161">來源語言<translation table></span><span class="sxs-lookup"><span data-stu-id="959d4-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="959d4-162">使用命令所命名的轉譯資料表來轉譯輸出。</span><span class="sxs-lookup"><span data-stu-id="959d4-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="959d4-163">BasicXml 和 NoComma 的轉譯資料表會隨附于 WMIC。</span><span class="sxs-lookup"><span data-stu-id="959d4-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="959d4-164">台<interval></span><span class="sxs-lookup"><span data-stu-id="959d4-164">/EVERY:<interval></span></span>              | <span data-ttu-id="959d4-165">每秒重複命令 <interval> 。</span><span class="sxs-lookup"><span data-stu-id="959d4-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="959d4-166">形式<format specifier></span><span class="sxs-lookup"><span data-stu-id="959d4-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="959d4-167">指定要格式化資料的關鍵單字或 XSL 檔案名。</span><span class="sxs-lookup"><span data-stu-id="959d4-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="959d4-168">範例： **進程 GET 名稱**</span><span class="sxs-lookup"><span data-stu-id="959d4-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-169"><span id="LIST"></span><span id="list"></span>清單</span><span class="sxs-lookup"><span data-stu-id="959d4-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="959d4-170">顯示資料。</span><span class="sxs-lookup"><span data-stu-id="959d4-170">Shows data.</span></span> <span data-ttu-id="959d4-171">LIST 是預設動詞。</span><span class="sxs-lookup"><span data-stu-id="959d4-171">LIST is the default verb.</span></span>

<span data-ttu-id="959d4-172">清單具有下列副詞。</span><span class="sxs-lookup"><span data-stu-id="959d4-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="959d4-173">副詞</span><span class="sxs-lookup"><span data-stu-id="959d4-173">Adverb</span></span>   | <span data-ttu-id="959d4-174">Description</span><span class="sxs-lookup"><span data-stu-id="959d4-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="959d4-175">簡短</span><span class="sxs-lookup"><span data-stu-id="959d4-175">BRIEF</span></span>    | <span data-ttu-id="959d4-176">屬性的核心集。</span><span class="sxs-lookup"><span data-stu-id="959d4-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="959d4-177">FULL</span><span class="sxs-lookup"><span data-stu-id="959d4-177">FULL</span></span>     | <span data-ttu-id="959d4-178">完整的屬性集。</span><span class="sxs-lookup"><span data-stu-id="959d4-178">Full set of properties.</span></span> <span data-ttu-id="959d4-179">這是清單的預設副詞。</span><span class="sxs-lookup"><span data-stu-id="959d4-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="959d4-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="959d4-180">INSTANCE</span></span> | <span data-ttu-id="959d4-181">僅限實例路徑。</span><span class="sxs-lookup"><span data-stu-id="959d4-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="959d4-182">狀態</span><span class="sxs-lookup"><span data-stu-id="959d4-182">STATUS</span></span>   | <span data-ttu-id="959d4-183">物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="959d4-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="959d4-184">系統</span><span class="sxs-lookup"><span data-stu-id="959d4-184">SYSTEM</span></span>   | <span data-ttu-id="959d4-185">系統屬性。</span><span class="sxs-lookup"><span data-stu-id="959d4-185">System properties.</span></span>                                           |



 

<span data-ttu-id="959d4-186">清單具有下列參數。</span><span class="sxs-lookup"><span data-stu-id="959d4-186">LIST has the following switches.</span></span>



| <span data-ttu-id="959d4-187">Switch</span><span class="sxs-lookup"><span data-stu-id="959d4-187">Switch</span></span>                               | <span data-ttu-id="959d4-188">描述</span><span class="sxs-lookup"><span data-stu-id="959d4-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959d4-189">來源語言<translation table></span><span class="sxs-lookup"><span data-stu-id="959d4-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="959d4-190">使用命令所命名的轉譯資料表來轉譯輸出。</span><span class="sxs-lookup"><span data-stu-id="959d4-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="959d4-191">BasicXml 和 NoComma 的轉譯資料表會隨附于 WMIC。</span><span class="sxs-lookup"><span data-stu-id="959d4-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="959d4-192">台<interval></span><span class="sxs-lookup"><span data-stu-id="959d4-192">/EVERY:<interval></span></span>              | <span data-ttu-id="959d4-193">每秒重複命令 <interval> 。</span><span class="sxs-lookup"><span data-stu-id="959d4-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="959d4-194">形式<format specifier></span><span class="sxs-lookup"><span data-stu-id="959d4-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="959d4-195">指定要格式化資料的關鍵單字或 XSL 檔案名。</span><span class="sxs-lookup"><span data-stu-id="959d4-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="959d4-196">範例： **流程清單簡介**</span><span class="sxs-lookup"><span data-stu-id="959d4-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-197"><span id="SET"></span><span id="set"></span>設置</span><span class="sxs-lookup"><span data-stu-id="959d4-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="959d4-198">將值指派給屬性。</span><span class="sxs-lookup"><span data-stu-id="959d4-198">Assigns values to properties.</span></span> <span data-ttu-id="959d4-199">範例： **環境集合名稱 = "TEMP"**， **VARIABLEVALUE = "NEW"**</span><span class="sxs-lookup"><span data-stu-id="959d4-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="959d4-200">交換器</span><span class="sxs-lookup"><span data-stu-id="959d4-200">Switches</span></span>

<span data-ttu-id="959d4-201">全域參數是用來設定 WMIC 環境的預設值。</span><span class="sxs-lookup"><span data-stu-id="959d4-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="959d4-202">您可以藉由輸入 **內容** 命令來查看這些參數所設定之條件的目前值。</span><span class="sxs-lookup"><span data-stu-id="959d4-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="959d4-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span><span class="sxs-lookup"><span data-stu-id="959d4-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-204">別名通常使用的命名空間。</span><span class="sxs-lookup"><span data-stu-id="959d4-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="959d4-205">預設值為根 \\ cimv2。</span><span class="sxs-lookup"><span data-stu-id="959d4-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="959d4-206">範例： **/NAMESPACE： \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="959d4-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span><span class="sxs-lookup"><span data-stu-id="959d4-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-208">命名空間 WMIC 通常會尋找別名和其他 WMIC 資訊。</span><span class="sxs-lookup"><span data-stu-id="959d4-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="959d4-209">範例： **/ROLE： \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="959d4-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span><span class="sxs-lookup"><span data-stu-id="959d4-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-211">電腦名稱稱（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="959d4-211">Computer names, comma delimited.</span></span> <span data-ttu-id="959d4-212">所有命令都會針對此值中列出的所有電腦進行同步執行。</span><span class="sxs-lookup"><span data-stu-id="959d4-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="959d4-213">檔案名前面必須加上 &。</span><span class="sxs-lookup"><span data-stu-id="959d4-213">File names must be prefixed with &.</span></span> <span data-ttu-id="959d4-214">檔案內的電腦名稱稱必須以逗號分隔，或在個別的行上。</span><span class="sxs-lookup"><span data-stu-id="959d4-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="959d4-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span><span class="sxs-lookup"><span data-stu-id="959d4-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="959d4-216">模擬等級。</span><span class="sxs-lookup"><span data-stu-id="959d4-216">Impersonation level.</span></span>

<span data-ttu-id="959d4-217">範例： **/IMPLEVEL： Anonymous**</span><span class="sxs-lookup"><span data-stu-id="959d4-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span><span class="sxs-lookup"><span data-stu-id="959d4-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="959d4-219">驗證層級。</span><span class="sxs-lookup"><span data-stu-id="959d4-219">Authentication level.</span></span>

<span data-ttu-id="959d4-220">範例： **/AUTHLEVEL： Pkt**</span><span class="sxs-lookup"><span data-stu-id="959d4-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="959d4-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-222">現場。</span><span class="sxs-lookup"><span data-stu-id="959d4-222">Locale.</span></span>

<span data-ttu-id="959d4-223">範例： **/LOCALE： MS \_ 411**</span><span class="sxs-lookup"><span data-stu-id="959d4-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="959d4-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="959d4-225">啟用或停用擁有權限。</span><span class="sxs-lookup"><span data-stu-id="959d4-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="959d4-226">範例： **/PRIVILEGES： ENABLE** 或 **/PRIVILEGES： DISABLE**</span><span class="sxs-lookup"><span data-stu-id="959d4-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span><span class="sxs-lookup"><span data-stu-id="959d4-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-228">顯示所有用來執行 WMIC 命令的函式的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="959d4-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="959d4-229">範例： **/TRACE： ON** 或 **/TRACE： OFF**</span><span class="sxs-lookup"><span data-stu-id="959d4-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span><span class="sxs-lookup"><span data-stu-id="959d4-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="959d4-231">記錄 XML 檔案的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="959d4-231">Records all output to an XML file.</span></span> <span data-ttu-id="959d4-232">輸出也會顯示在命令提示字元中。</span><span class="sxs-lookup"><span data-stu-id="959d4-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="959d4-233">範例： **/RECORD：** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="959d4-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="959d4-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="959d4-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-235">通常會確認刪除命令。</span><span class="sxs-lookup"><span data-stu-id="959d4-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="959d4-236">範例： **/INTERACTIVE： ON** 或 **/INTERACTIVE： OFF**</span><span class="sxs-lookup"><span data-stu-id="959d4-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on** \| **off** \| *TimeoutInMilliseconds*</span><span class="sxs-lookup"><span data-stu-id="959d4-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="959d4-238">如果在/NODE 電腦上，會在傳送 WMIC 命令給它們之前進行 ping。</span><span class="sxs-lookup"><span data-stu-id="959d4-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="959d4-239">如果電腦沒有回應，就不會將這些命令傳送給它。</span><span class="sxs-lookup"><span data-stu-id="959d4-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="959d4-240">範例： "/FAILFAST： ON" 或 "/FAILFAST： OFF"</span><span class="sxs-lookup"><span data-stu-id="959d4-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="959d4-241">**WMIC/FAILFAST：1000**</span><span class="sxs-lookup"><span data-stu-id="959d4-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-242"><span id="_USER"></span><span id="_user"></span>/USER</span><span class="sxs-lookup"><span data-stu-id="959d4-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="959d4-243">當存取/NODE 電腦或別名中所指定的電腦時，由 WMIC 使用的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="959d4-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="959d4-244">系統會提示您輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="959d4-244">You are prompted for the password.</span></span> <span data-ttu-id="959d4-245">使用者名稱不能與本機電腦搭配使用。</span><span class="sxs-lookup"><span data-stu-id="959d4-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="959d4-246">範例： **/user：**_JSMITH_</span><span class="sxs-lookup"><span data-stu-id="959d4-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="959d4-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span><span class="sxs-lookup"><span data-stu-id="959d4-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="959d4-248">WMIC 在存取/NODE 電腦時所使用的密碼。</span><span class="sxs-lookup"><span data-stu-id="959d4-248">Password used by WMIC when accessing the /NODE computers.</span></span> <span data-ttu-id="959d4-249">在命令列可以看到密碼。</span><span class="sxs-lookup"><span data-stu-id="959d4-249">The password is visible at the command line.</span></span>

<span data-ttu-id="959d4-250">範例： **/password：**_PASSWORD_</span><span class="sxs-lookup"><span data-stu-id="959d4-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="959d4-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span><span class="sxs-lookup"><span data-stu-id="959d4-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="959d4-252">指定所有輸出重新導向的模式。</span><span class="sxs-lookup"><span data-stu-id="959d4-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="959d4-253">輸出不會出現在命令列中，而且會在開始輸出之前清除目的地。</span><span class="sxs-lookup"><span data-stu-id="959d4-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="959d4-254">有效的值為 STDOUT、剪貼簿或檔案名。</span><span class="sxs-lookup"><span data-stu-id="959d4-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="959d4-255">範例： **/OUTPUT：剪貼** 簿</span><span class="sxs-lookup"><span data-stu-id="959d4-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span><span class="sxs-lookup"><span data-stu-id="959d4-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="959d4-257">指定所有輸出重新導向的模式。</span><span class="sxs-lookup"><span data-stu-id="959d4-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="959d4-258">輸出不會出現在命令列中，而且不會在開始輸出之前清除目的地，並且會將輸出附加至目的地目前內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="959d4-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="959d4-259">有效的值為 STDOUT、剪貼簿或檔案名。</span><span class="sxs-lookup"><span data-stu-id="959d4-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="959d4-260">範例： **/APPEND：剪貼** 簿</span><span class="sxs-lookup"><span data-stu-id="959d4-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span><span class="sxs-lookup"><span data-stu-id="959d4-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="959d4-262">搭配 **LIST** 和 **GET/EVERY** 參數使用。</span><span class="sxs-lookup"><span data-stu-id="959d4-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="959d4-263">如果匯總為 ON，當/NODE 中的所有電腦都已回應或超時時，LIST 和 GET 會顯示其結果。如果匯總為 OFF，則會在收到結果時立即列出並顯示其結果。</span><span class="sxs-lookup"><span data-stu-id="959d4-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="959d4-264">範例： **/AGGREGATE： OFF** 或 **/AGGREGATE： ON**</span><span class="sxs-lookup"><span data-stu-id="959d4-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="959d4-265">命令</span><span class="sxs-lookup"><span data-stu-id="959d4-265">Commands</span></span>

<span data-ttu-id="959d4-266">下列 WMIC 命令隨時都可供使用。</span><span class="sxs-lookup"><span data-stu-id="959d4-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="959d4-267">如需詳細資訊，請參閱 [WMIC 命令](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="959d4-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="959d4-268"><span id="CLASS"></span><span id="class"></span>類</span><span class="sxs-lookup"><span data-stu-id="959d4-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="959d4-269">從預設的 WMIC 別名模式進行 Escape，以直接存取 WMI 架構中的類別。</span><span class="sxs-lookup"><span data-stu-id="959d4-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="959d4-270">如需可用 WMI 類別的詳細資訊，請參閱 [Wmi 類別](wmi-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="959d4-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="959d4-271">範例： **WMIC/OUTPUT： c： \\ClassOutput.htm 類別 Win32 \_ SoundDevice**</span><span class="sxs-lookup"><span data-stu-id="959d4-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-272"><span id="PATH"></span><span id="path"></span>路徑</span><span class="sxs-lookup"><span data-stu-id="959d4-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="959d4-273">從預設的 WMIC 別名模式進行 Escape，以直接存取 WMI 架構中的實例。</span><span class="sxs-lookup"><span data-stu-id="959d4-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="959d4-274">範例： **WMIC/OUTPUT： c： \\PathOutput.txt PATH WIN32 \_ SoundDevice GET/VALUE**</span><span class="sxs-lookup"><span data-stu-id="959d4-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-275"><span id="CONTEXT"></span><span id="context"></span>上下文</span><span class="sxs-lookup"><span data-stu-id="959d4-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="959d4-276">顯示所有全域參數的目前值。</span><span class="sxs-lookup"><span data-stu-id="959d4-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="959d4-277">範例： **WMIC 內容**</span><span class="sxs-lookup"><span data-stu-id="959d4-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-278"><span id="QUIT"></span><span id="quit"></span>退出</span><span class="sxs-lookup"><span data-stu-id="959d4-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="959d4-279">退出 WMIC。</span><span class="sxs-lookup"><span data-stu-id="959d4-279">Exit from WMIC.</span></span>

<span data-ttu-id="959d4-280">範例： **WMIC QUIT**</span><span class="sxs-lookup"><span data-stu-id="959d4-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="959d4-281"><span id="EXIT"></span><span id="exit"></span>退出</span><span class="sxs-lookup"><span data-stu-id="959d4-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="959d4-282">退出 WMIC。</span><span class="sxs-lookup"><span data-stu-id="959d4-282">Exit from WMIC.</span></span>

<span data-ttu-id="959d4-283">範例： **WMIC EXIT**</span><span class="sxs-lookup"><span data-stu-id="959d4-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="959d4-284">範例</span><span class="sxs-lookup"><span data-stu-id="959d4-284">Examples</span></span>

<span data-ttu-id="959d4-285">使用 TechNet 資源庫上的 [wmic 範例設定 ip/子網/閘道/dns 的腳本](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) ，說明如何修改和更新 Ip、子網、閘道和 dns 設定。</span><span class="sxs-lookup"><span data-stu-id="959d4-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="959d4-286">規格需求</span><span class="sxs-lookup"><span data-stu-id="959d4-286">Requirements</span></span>



| <span data-ttu-id="959d4-287">需求</span><span class="sxs-lookup"><span data-stu-id="959d4-287">Requirement</span></span> | <span data-ttu-id="959d4-288">值</span><span class="sxs-lookup"><span data-stu-id="959d4-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="959d4-289">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="959d4-289">Minimum supported client</span></span><br/> | <span data-ttu-id="959d4-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="959d4-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="959d4-291">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="959d4-291">Minimum supported server</span></span><br/> | <span data-ttu-id="959d4-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="959d4-292">Windows Server 2008</span></span><br/> |



 

