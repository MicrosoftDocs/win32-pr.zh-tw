---
description: 使用資料表編輯器（例如 Orca 或 SQL 查詢），修改 MNPFren.msi 資料庫中任何其他可當地語系化的資料行。
ms.assetid: b62cf529-71a0-47ff-99ea-a182c0fe4479
title: 當地語系化資料庫資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed36b1adb2c496c9019b482c929e449187b1e0bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027021"
---
# <a name="localizing-database-columns"></a><span data-ttu-id="73eb3-103">當地語系化資料庫資料行</span><span class="sxs-lookup"><span data-stu-id="73eb3-103">Localizing Database Columns</span></span>

<span data-ttu-id="73eb3-104">使用資料表編輯器（例如 Orca 或 SQL 查詢），修改 MNPFren.msi 資料庫中任何其他可當地語系化的資料行。</span><span class="sxs-lookup"><span data-stu-id="73eb3-104">Modify any of the other localizable columns in the MNPFren.msi database using a table editor such as Orca or SQL queries.</span></span> <span data-ttu-id="73eb3-105">若要判斷特定資料表的哪些資料行可以當地語系化成另一種語言，請參閱該資料庫資料表的參考主題。</span><span class="sxs-lookup"><span data-stu-id="73eb3-105">To determine which columns of a particular table may be localized to another language, see the reference topic for that database table.</span></span> <span data-ttu-id="73eb3-106">請參閱 [資料庫資料表](database-tables.md) ，以取得所有資料庫資料表的清單。</span><span class="sxs-lookup"><span data-stu-id="73eb3-106">See [Database Tables](database-tables.md) for a list of all database tables.</span></span>

<span data-ttu-id="73eb3-107">例如， [控制資料表](control-table.md) 中某些記錄的文字欄位可能需要當地語系化為法文。</span><span class="sxs-lookup"><span data-stu-id="73eb3-107">For example, the Text field of some records in the [Control table](control-table.md) may need to be localized into French.</span></span> <span data-ttu-id="73eb3-108">字串「您確定要取消 \[ ProductName \] 安裝嗎？」</span><span class="sxs-lookup"><span data-stu-id="73eb3-108">The string "Are you sure you want to cancel \[ProductName\] installation?"</span></span> <span data-ttu-id="73eb3-109">在此資料表中，您可以修改 [ [取消] 對話方塊](cancel-dialog.md) 中的，以法文顯示。</span><span class="sxs-lookup"><span data-stu-id="73eb3-109">in the [Cancel Dialog](cancel-dialog.md) may be modified in this table to be displayed in French.</span></span> <span data-ttu-id="73eb3-110">.Msi 檔案中的原始記錄會如下所示。</span><span class="sxs-lookup"><span data-stu-id="73eb3-110">The original record in .msi file appears as follows.</span></span>

<span data-ttu-id="73eb3-111">[控制資料表](control-table.md) (原始 .msi 檔案的部分) </span><span class="sxs-lookup"><span data-stu-id="73eb3-111">[Control Table](control-table.md) (partial) of the original .msi file</span></span>



| <span data-ttu-id="73eb3-112">對話\_</span><span class="sxs-lookup"><span data-stu-id="73eb3-112">Dialog\_</span></span>  | <span data-ttu-id="73eb3-113">控制</span><span class="sxs-lookup"><span data-stu-id="73eb3-113">Control</span></span> | <span data-ttu-id="73eb3-114">類型</span><span class="sxs-lookup"><span data-stu-id="73eb3-114">Type</span></span> | <span data-ttu-id="73eb3-115">X</span><span class="sxs-lookup"><span data-stu-id="73eb3-115">X</span></span>   | <span data-ttu-id="73eb3-116">Y</span><span class="sxs-lookup"><span data-stu-id="73eb3-116">Y</span></span>   | <span data-ttu-id="73eb3-117">寬度</span><span class="sxs-lookup"><span data-stu-id="73eb3-117">Width</span></span> | <span data-ttu-id="73eb3-118">高度</span><span class="sxs-lookup"><span data-stu-id="73eb3-118">Height</span></span> | <span data-ttu-id="73eb3-119">屬性</span><span class="sxs-lookup"><span data-stu-id="73eb3-119">Attributes</span></span> | <span data-ttu-id="73eb3-120">屬性</span><span class="sxs-lookup"><span data-stu-id="73eb3-120">Property</span></span> | <span data-ttu-id="73eb3-121">Text</span><span class="sxs-lookup"><span data-stu-id="73eb3-121">Text</span></span>                                                          | <span data-ttu-id="73eb3-122">控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="73eb3-122">Control\_Next</span></span> | <span data-ttu-id="73eb3-123">Help</span><span class="sxs-lookup"><span data-stu-id="73eb3-123">Help</span></span> |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------|---------------|------|
| <span data-ttu-id="73eb3-124">CancelDlg</span><span class="sxs-lookup"><span data-stu-id="73eb3-124">CancelDlg</span></span> | <span data-ttu-id="73eb3-125">Text</span><span class="sxs-lookup"><span data-stu-id="73eb3-125">Text</span></span>    | <span data-ttu-id="73eb3-126">Text</span><span class="sxs-lookup"><span data-stu-id="73eb3-126">Text</span></span> | <span data-ttu-id="73eb3-127">48</span><span class="sxs-lookup"><span data-stu-id="73eb3-127">48</span></span>  | <span data-ttu-id="73eb3-128">15</span><span class="sxs-lookup"><span data-stu-id="73eb3-128">15</span></span>  | <span data-ttu-id="73eb3-129">194</span><span class="sxs-lookup"><span data-stu-id="73eb3-129">194</span></span>   | <span data-ttu-id="73eb3-130">30</span><span class="sxs-lookup"><span data-stu-id="73eb3-130">30</span></span>     | <span data-ttu-id="73eb3-131">3</span><span class="sxs-lookup"><span data-stu-id="73eb3-131">3</span></span>          |          | <span data-ttu-id="73eb3-132">確定要取消 \[ ProductName \] 安裝嗎？</span><span class="sxs-lookup"><span data-stu-id="73eb3-132">Are you sure you want to cancel \[ProductName\] installation?</span></span> |               |      |



 

<span data-ttu-id="73eb3-133">您可以使用資料表編輯器來修改文字欄位，例如 SDK 所提供的 Orca 資料表編輯器或其他資料表編輯器，或使用 SQL 查詢來變更控制資料表記錄的文字欄位。</span><span class="sxs-lookup"><span data-stu-id="73eb3-133">You may use a table editor to modify the Text field, such as the Orca table editor provided with the SDK or another table editor, or use a SQL query to change the Text field of the Control table record.</span></span> <span data-ttu-id="73eb3-134">在 Windows Installer SDK 中，會以公用程式 WiRunSQL.vbs 的形式提供示範腳本驅動資料庫查詢的範例。</span><span class="sxs-lookup"><span data-stu-id="73eb3-134">An example demonstrating script-driven database queries is provided in the Windows Installer SDK as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="73eb3-135">使用下列命令列，以 WiRunSQL.vbs 和 Windows Script Host 來修改欄位。</span><span class="sxs-lookup"><span data-stu-id="73eb3-135">Use the following command line to modify the field with WiRunSQL.vbs and the Windows Script Host.</span></span> <span data-ttu-id="73eb3-136">另請參閱 [使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。</span><span class="sxs-lookup"><span data-stu-id="73eb3-136">See also [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

<span data-ttu-id="73eb3-137">**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control. Text = ' Etes-vous sur de vouloir annuler l'installation de \[ ProductName \] ？ 'WHERE Control. Dialog \_ = ' CancelDlg '，control = ' Text ' "**</span><span class="sxs-lookup"><span data-stu-id="73eb3-137">**Cscript WiRunSQL.vbs MNPFren.msi "UPDATE Control SET Control.Text='Etes-vous sur de vouloir annuler l'installation de \[ProductName\]?' WHERE Control.Dialog\_='CancelDlg' AND Control.Control='Text'"**</span></span>

<span data-ttu-id="73eb3-138">MNPFren.msi 中 (部分) 的[控制項資料表](control-table.md)</span><span class="sxs-lookup"><span data-stu-id="73eb3-138">[Control Table](control-table.md) (partial) in MNPFren.msi</span></span>



| <span data-ttu-id="73eb3-139">對話\_</span><span class="sxs-lookup"><span data-stu-id="73eb3-139">Dialog\_</span></span>  | <span data-ttu-id="73eb3-140">控制</span><span class="sxs-lookup"><span data-stu-id="73eb3-140">Control</span></span> | <span data-ttu-id="73eb3-141">類型</span><span class="sxs-lookup"><span data-stu-id="73eb3-141">Type</span></span> | <span data-ttu-id="73eb3-142">X</span><span class="sxs-lookup"><span data-stu-id="73eb3-142">X</span></span>   | <span data-ttu-id="73eb3-143">Y</span><span class="sxs-lookup"><span data-stu-id="73eb3-143">Y</span></span>   | <span data-ttu-id="73eb3-144">寬度</span><span class="sxs-lookup"><span data-stu-id="73eb3-144">Width</span></span> | <span data-ttu-id="73eb3-145">高度</span><span class="sxs-lookup"><span data-stu-id="73eb3-145">Height</span></span> | <span data-ttu-id="73eb3-146">屬性</span><span class="sxs-lookup"><span data-stu-id="73eb3-146">Attributes</span></span> | <span data-ttu-id="73eb3-147">屬性</span><span class="sxs-lookup"><span data-stu-id="73eb3-147">Property</span></span> | <span data-ttu-id="73eb3-148">Text</span><span class="sxs-lookup"><span data-stu-id="73eb3-148">Text</span></span>                                                                | <span data-ttu-id="73eb3-149">控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="73eb3-149">Control\_Next</span></span> | <span data-ttu-id="73eb3-150">Help</span><span class="sxs-lookup"><span data-stu-id="73eb3-150">Help</span></span> |
|-----------|---------|------|-----|-----|-------|--------|------------|----------|---------------------------------------------------------------------|---------------|------|
| <span data-ttu-id="73eb3-151">CancelDlg</span><span class="sxs-lookup"><span data-stu-id="73eb3-151">CancelDlg</span></span> | <span data-ttu-id="73eb3-152">Text</span><span class="sxs-lookup"><span data-stu-id="73eb3-152">Text</span></span>    | <span data-ttu-id="73eb3-153">Text</span><span class="sxs-lookup"><span data-stu-id="73eb3-153">Text</span></span> | <span data-ttu-id="73eb3-154">48</span><span class="sxs-lookup"><span data-stu-id="73eb3-154">48</span></span>  | <span data-ttu-id="73eb3-155">15</span><span class="sxs-lookup"><span data-stu-id="73eb3-155">15</span></span>  | <span data-ttu-id="73eb3-156">194</span><span class="sxs-lookup"><span data-stu-id="73eb3-156">194</span></span>   | <span data-ttu-id="73eb3-157">30</span><span class="sxs-lookup"><span data-stu-id="73eb3-157">30</span></span>     | <span data-ttu-id="73eb3-158">3</span><span class="sxs-lookup"><span data-stu-id="73eb3-158">3</span></span>          |          | <span data-ttu-id="73eb3-159">Êtes-vous sûr de vouloir annuler l'installation de \[ ProductName \] ？</span><span class="sxs-lookup"><span data-stu-id="73eb3-159">Êtes-vous sûr de vouloir annuler l'installation de \[ProductName\]?</span></span> |               |      |



 

<span data-ttu-id="73eb3-160">如果使用者取消安裝 MNPFren.msi，[ **取消] 對話方塊** 隨即出現，並顯示下列文字： "Êtes-vous sûr de vouloir annuler L'INSTALLATION de MNP2000？"</span><span class="sxs-lookup"><span data-stu-id="73eb3-160">If the installation of MNPFren.msi is canceled by the user, the **Cancel Dialog** appears displaying the text: "Êtes-vous sûr de vouloir annuler l'installation de MNP2000?"</span></span>

<span data-ttu-id="73eb3-161">使用這個方法將 UI 文字當地語系化成不同的語言時，必須測試當地語系化的 UI，以確保控制項的大小夠大，足以顯示整個當地語系化的文字。</span><span class="sxs-lookup"><span data-stu-id="73eb3-161">When using this method to localize UI text to a different language, the localized UI must be tested to ensure that the size of controls are large enough to display the entire localized text.</span></span> <span data-ttu-id="73eb3-162">這應該使用可供顯示的所有字型大小設定進行測試。</span><span class="sxs-lookup"><span data-stu-id="73eb3-162">This should be tested using all font size settings that are available for display.</span></span> <span data-ttu-id="73eb3-163">當地語系化的文字可能需要比原始文字更多的空間，如果顯示在太小的控制項中，可能會被截斷。</span><span class="sxs-lookup"><span data-stu-id="73eb3-163">Localized text can require more space than the original text and may be truncated if displayed in a control that is too small.</span></span>

[<span data-ttu-id="73eb3-164">繼續</span><span class="sxs-lookup"><span data-stu-id="73eb3-164">Continue</span></span>](updating-productlanguage-and-productcode-properties.md)

 

 



