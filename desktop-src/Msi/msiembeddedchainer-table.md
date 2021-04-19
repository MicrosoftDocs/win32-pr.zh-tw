---
description: 您可以使用此資料表來撰寫多套件安裝。
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: MsiEmbeddedChainer 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980790"
---
# <a name="msiembeddedchainer-table"></a><span data-ttu-id="46deb-103">MsiEmbeddedChainer 資料表</span><span class="sxs-lookup"><span data-stu-id="46deb-103">MsiEmbeddedChainer Table</span></span>

<span data-ttu-id="46deb-104">您可以使用此資料表來撰寫 [多套件安裝](multiple-package-installations.md)。</span><span class="sxs-lookup"><span data-stu-id="46deb-104">Use this table to author a [multiple-package installation](multiple-package-installations.md).</span></span> <span data-ttu-id="46deb-105">MsiEmbeddedChainer 資料表中的每個資料列都會參考不同的使用者定義函數，可用來從單一封裝安裝多個 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="46deb-105">Each row in the MsiEmbeddedChainer table references a different user-defined function that can be used to install multiple Windows Installer packages from a single package.</span></span> <span data-ttu-id="46deb-106">使用者定義函數的 [可執行檔](executable-files.md) 會儲存在 Windows Installer 套件內。</span><span class="sxs-lookup"><span data-stu-id="46deb-106">The [executable files](executable-files.md) for the user-defined functions are stored inside the Windows Installer package.</span></span>

<span data-ttu-id="46deb-107">**[Windows Installer 4.0 或更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-107">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="46deb-108">從 Windows Installer 4.5 開始，可以使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="46deb-108">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="46deb-109">**啟用 [遠端桌面服務](../termserv/terminal-services-portal.md) 角色的 Windows Server 2008 R2：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-109">**Windows Server 2008 R2 with the [Remote Desktop Services](../termserv/terminal-services-portal.md) role enabled:** Not supported.</span></span> <span data-ttu-id="46deb-110">如果啟用 [遠端桌面服務](../termserv/terminal-services-portal.md) 角色，使用 MsiEmbeddedChainer 資料表的多個套件安裝將會失敗。</span><span class="sxs-lookup"><span data-stu-id="46deb-110">A multiple package installation using the MsiEmbeddedChainer table fails if the [Remote Desktop Services](../termserv/terminal-services-portal.md) role is enabled.</span></span>

<span data-ttu-id="46deb-111">若要從單一封裝安裝多個封裝，MsiEmbeddedChainer 資料表中所列的其中一個使用者定義函數必須在評估為執行動作的條件欄位中具有條件陳述式。</span><span class="sxs-lookup"><span data-stu-id="46deb-111">To install multiple packages from a single package, one of the user-defined functions listed in the MsiEmbeddedChainer table must have a conditional statment in the Condition field that evaluates to run the action.</span></span> <span data-ttu-id="46deb-112">如果有一個以上的函式具有評估為執行的條件，則只能執行一個函數。</span><span class="sxs-lookup"><span data-stu-id="46deb-112">If more than one function has a condition that evaluates to run, only one function can run.</span></span> <span data-ttu-id="46deb-113">這種情況是錯誤，無法保證將會執行哪些函數。</span><span class="sxs-lookup"><span data-stu-id="46deb-113">This case is an error, and it cannot be guaranteed which function will run.</span></span> <span data-ttu-id="46deb-114">如果安裝需要其他自訂動作，則應該在 [CustomAction 資料表](customaction-table.md) 和順序資料表中撰寫這些動作。</span><span class="sxs-lookup"><span data-stu-id="46deb-114">If other custom actions are needed by the installation, these should be authored into the [CustomAction table](customaction-table.md) and sequence tables.</span></span>

<span data-ttu-id="46deb-115">這些函式必須藉由呼叫 [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) 函式來加入目前的安裝，而且必須呼叫 [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) 函數來認可多個封裝的安裝。</span><span class="sxs-lookup"><span data-stu-id="46deb-115">The functions must join the current installation by calling the [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) function and must call the [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) function to commit the installation of multiple packages.</span></span> <span data-ttu-id="46deb-116">如果函式在呼叫 **MsiEndTransaction** 之前傳回，安裝程式會復原所有安裝。</span><span class="sxs-lookup"><span data-stu-id="46deb-116">If the functions return before calling **MsiEndTransaction**, the installer rolls back all installations.</span></span>

<span data-ttu-id="46deb-117">MsiEmbeddedChainer 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="46deb-117">The MsiEmbeddedChainer table has the following columns.</span></span>



| <span data-ttu-id="46deb-118">Column</span><span class="sxs-lookup"><span data-stu-id="46deb-118">Column</span></span>             | <span data-ttu-id="46deb-119">類型</span><span class="sxs-lookup"><span data-stu-id="46deb-119">Type</span></span>                             | <span data-ttu-id="46deb-120">答案</span><span class="sxs-lookup"><span data-stu-id="46deb-120">Key</span></span> | <span data-ttu-id="46deb-121">Nullable</span><span class="sxs-lookup"><span data-stu-id="46deb-121">Nullable</span></span> |
|--------------------|----------------------------------|-----|----------|
| <span data-ttu-id="46deb-122">MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="46deb-122">MsiEmbeddedChainer</span></span> | [<span data-ttu-id="46deb-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="46deb-123">Identifier</span></span>](identifier.md)     | <span data-ttu-id="46deb-124">Y</span><span class="sxs-lookup"><span data-stu-id="46deb-124">Y</span></span>   | <span data-ttu-id="46deb-125">N</span><span class="sxs-lookup"><span data-stu-id="46deb-125">N</span></span>        |
| <span data-ttu-id="46deb-126">條件</span><span class="sxs-lookup"><span data-stu-id="46deb-126">Condition</span></span>          | [<span data-ttu-id="46deb-127">Condition</span><span class="sxs-lookup"><span data-stu-id="46deb-127">Condition</span></span>](condition.md)       | <span data-ttu-id="46deb-128">N</span><span class="sxs-lookup"><span data-stu-id="46deb-128">N</span></span>   | <span data-ttu-id="46deb-129">Y</span><span class="sxs-lookup"><span data-stu-id="46deb-129">Y</span></span>        |
| <span data-ttu-id="46deb-130">CommandLine</span><span class="sxs-lookup"><span data-stu-id="46deb-130">CommandLine</span></span>        | [<span data-ttu-id="46deb-131">格式 化</span><span class="sxs-lookup"><span data-stu-id="46deb-131">Formatted</span></span>](formatted.md)       | <span data-ttu-id="46deb-132">N</span><span class="sxs-lookup"><span data-stu-id="46deb-132">N</span></span>   | <span data-ttu-id="46deb-133">Y</span><span class="sxs-lookup"><span data-stu-id="46deb-133">Y</span></span>        |
| <span data-ttu-id="46deb-134">來源</span><span class="sxs-lookup"><span data-stu-id="46deb-134">Source</span></span>             | [<span data-ttu-id="46deb-135">CustomSource</span><span class="sxs-lookup"><span data-stu-id="46deb-135">CustomSource</span></span>](customsource.md) | <span data-ttu-id="46deb-136">N</span><span class="sxs-lookup"><span data-stu-id="46deb-136">N</span></span>   | <span data-ttu-id="46deb-137">N</span><span class="sxs-lookup"><span data-stu-id="46deb-137">N</span></span>        |
| <span data-ttu-id="46deb-138">類型</span><span class="sxs-lookup"><span data-stu-id="46deb-138">Type</span></span>               | [<span data-ttu-id="46deb-139">整數</span><span class="sxs-lookup"><span data-stu-id="46deb-139">Integer</span></span>](integer.md)           | <span data-ttu-id="46deb-140">N</span><span class="sxs-lookup"><span data-stu-id="46deb-140">N</span></span>   | <span data-ttu-id="46deb-141">N</span><span class="sxs-lookup"><span data-stu-id="46deb-141">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="46deb-142">資料行</span><span class="sxs-lookup"><span data-stu-id="46deb-142">Columns</span></span>

<dl> <dt>

<span data-ttu-id="46deb-143"><span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="46deb-143"><span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer</span></span>
</dt> <dd>

<span data-ttu-id="46deb-144">資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="46deb-144">The primary key for the table.</span></span> <span data-ttu-id="46deb-145">這個值是這個資料列所描述的使用者定義函數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="46deb-145">This value is a unique identifier for the user-defined function described by this row.</span></span>

</dd> <dt>

<span data-ttu-id="46deb-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="46deb-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="46deb-147">執行使用者定義函數的條件陳述式。</span><span class="sxs-lookup"><span data-stu-id="46deb-147">A conditional statement for running the user-defined function.</span></span> <span data-ttu-id="46deb-148">您可以啟用或停用 MsiEmbeddedChainer 資料表中所列的函式，並使用會修改此欄位所評估之屬性值的轉換。</span><span class="sxs-lookup"><span data-stu-id="46deb-148">You can enable or disable the functions listed in the MsiEmbeddedChainer table using a transform that modifies property values evaluated by this field.</span></span> <span data-ttu-id="46deb-149">如需詳細資訊，請參閱 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。</span><span class="sxs-lookup"><span data-stu-id="46deb-149">For more information, see [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

</dd> <dt>

<span data-ttu-id="46deb-150"><span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>命令</span><span class="sxs-lookup"><span data-stu-id="46deb-150"><span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>CommandLine</span></span>
</dt> <dd>

<span data-ttu-id="46deb-151">此欄位中的值是傳遞至來源資料行中所識別之可執行檔的命令列字串的一部分。</span><span class="sxs-lookup"><span data-stu-id="46deb-151">The value in this field is a part of the command line string passed to the executable file identified in the Source column.</span></span> <span data-ttu-id="46deb-152">安裝程式會將此欄位中的值附加至交易控制碼，以產生命令列。</span><span class="sxs-lookup"><span data-stu-id="46deb-152">The installer appends the value in this field to the transaction handle to generate the command line.</span></span> <span data-ttu-id="46deb-153">如果此資料行中的值為 null，則命令列只會包含交易控制碼。</span><span class="sxs-lookup"><span data-stu-id="46deb-153">If the value in this column is null, the command line consists of only the transaction handle.</span></span>

</dd> <dt>

<span data-ttu-id="46deb-154"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源</span><span class="sxs-lookup"><span data-stu-id="46deb-154"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="46deb-155">使用者定義函數之可執行檔的位置。</span><span class="sxs-lookup"><span data-stu-id="46deb-155">The location of the executable file for the user-defined function.</span></span> <span data-ttu-id="46deb-156">如果 [類型] 資料行中的值是2，這個資料行就可以將外部索引鍵包含在 [二進位資料表](binary-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="46deb-156">If the value in the Type column is 2, this column can contain an external key into the [Binary table](binary-table.md).</span></span> <span data-ttu-id="46deb-157">如果 Type 資料行中的值為18，則這個資料行可以在檔案 [資料表](file-table.md)中包含外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="46deb-157">If the value in the Type column is 18, this column can contain an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="46deb-158">如果 Type 資料行中的值為50，則這個資料行可以在 [屬性工作表](property-table.md)中包含外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="46deb-158">If the value in the Type column is 50, this column can contain an external key into the [Property table](property-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="46deb-159"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型</span><span class="sxs-lookup"><span data-stu-id="46deb-159"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="46deb-160">MsiEmbeddedChainer 資料表中所列的函式會使用下列自訂動作數數值型別來描述。</span><span class="sxs-lookup"><span data-stu-id="46deb-160">The functions listed in the MsiEmbeddedChainer table are described using the following custom action numeric types.</span></span> <span data-ttu-id="46deb-161">此資料行只能包含下列三個數數值型別的值：自訂動作旗標的任何其他組合都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="46deb-161">This column can contain the values for the following three numeric types only; any other combination of custom action flags is ignored.</span></span>



| <span data-ttu-id="46deb-162">自訂動作類型</span><span class="sxs-lookup"><span data-stu-id="46deb-162">Custom action type</span></span>                                 | <span data-ttu-id="46deb-163">自訂動作旗標</span><span class="sxs-lookup"><span data-stu-id="46deb-163">Custom action flags</span></span>                                                | <span data-ttu-id="46deb-164">十六進位</span><span class="sxs-lookup"><span data-stu-id="46deb-164">Hexadecimal</span></span> | <span data-ttu-id="46deb-165">Decimal</span><span class="sxs-lookup"><span data-stu-id="46deb-165">Decimal</span></span> |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [<span data-ttu-id="46deb-166">自訂動作類型2</span><span class="sxs-lookup"><span data-stu-id="46deb-166">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="46deb-167">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="46deb-167">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="46deb-168">0x002</span><span class="sxs-lookup"><span data-stu-id="46deb-168">0x002</span></span>       | <span data-ttu-id="46deb-169">2</span><span class="sxs-lookup"><span data-stu-id="46deb-169">2</span></span>       |
| [<span data-ttu-id="46deb-170">自訂動作類型18</span><span class="sxs-lookup"><span data-stu-id="46deb-170">Custom Action Type 18</span></span>](custom-action-type-18.md) | <span data-ttu-id="46deb-171">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="46deb-171">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="46deb-172">0x012</span><span class="sxs-lookup"><span data-stu-id="46deb-172">0x012</span></span>       | <span data-ttu-id="46deb-173">18</span><span class="sxs-lookup"><span data-stu-id="46deb-173">18</span></span>      |
| [<span data-ttu-id="46deb-174">自訂動作類型50</span><span class="sxs-lookup"><span data-stu-id="46deb-174">Custom Action Type 50</span></span>](custom-action-type-50.md) | <span data-ttu-id="46deb-175">**msidbCustomActionTypeExe**  + **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="46deb-175">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span>   | <span data-ttu-id="46deb-176">0x032</span><span class="sxs-lookup"><span data-stu-id="46deb-176">0x032</span></span>       | <span data-ttu-id="46deb-177">50</span><span class="sxs-lookup"><span data-stu-id="46deb-177">50</span></span>      |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46deb-178">備註</span><span class="sxs-lookup"><span data-stu-id="46deb-178">Remarks</span></span>

<span data-ttu-id="46deb-179">Windows Installer 不會防止此資料表中的使用者定義函式在應用程式的公告期間執行。</span><span class="sxs-lookup"><span data-stu-id="46deb-179">The Windows Installer does not prevent the user-defined functions in this table from running during the advertisement of the application.</span></span> <span data-ttu-id="46deb-180">您可以在 [條件] 資料行中使用條件陳述式，以防止函數在公告期間執行。</span><span class="sxs-lookup"><span data-stu-id="46deb-180">You can use a conditional statement in the Condition column to prevent a function from being run during advertisement.</span></span>

<span data-ttu-id="46deb-181">Windows Installer 也提供非內嵌的外部 UI 處理常式，可在 Windows Installer 封裝之上建立豐富的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="46deb-181">The Windows Installer also provides a non-embedded external UI handler to build a rich user interface on top of the Windows Installer package.</span></span> <span data-ttu-id="46deb-182">如需有關使用外部 UI 處理常式搭配 Windows Installer 的詳細資訊，請參閱 [使用 MsiSetExternalUI 監視安裝](monitoring-an-installation-using-msisetexternalui.md)。</span><span class="sxs-lookup"><span data-stu-id="46deb-182">For more information about using an external UI handler with the Windows Installer, see [Monitoring an Installation Using MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).</span></span>

<span data-ttu-id="46deb-183">[MsiPackageCertificate 資料表](msipackagecertificate-table.md)會列出數位簽章憑證，用來驗證進行多套件安裝之安裝套件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="46deb-183">The [MsiPackageCertificate Table](msipackagecertificate-table.md) lists digital signature certificates used to verify the identity of the installation packages that make a multiple-package installation.</span></span> <span data-ttu-id="46deb-184">您可以使用此表格來減少多套件安裝在需要系統管理員回應的 (UAC) 提示字元中，顯示 [*使用者帳戶控制*](u-gly.md) 的次數。</span><span class="sxs-lookup"><span data-stu-id="46deb-184">You can use this table to reduce the number of times your multiple-package installation displays a [*User Account Control*](u-gly.md) (UAC) prompt that requires a response by an administrator.</span></span>

 

 
