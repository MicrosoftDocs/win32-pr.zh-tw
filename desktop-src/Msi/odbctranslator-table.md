---
description: ODBCTranslator 資料表會列出屬於安裝的 ODBC 轉譯。
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: ODBCTranslator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001447"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="52774-103">ODBCTranslator 資料表</span><span class="sxs-lookup"><span data-stu-id="52774-103">ODBCTranslator Table</span></span>

<span data-ttu-id="52774-104">ODBCTranslator 資料表會列出屬於安裝的 ODBC 轉譯。</span><span class="sxs-lookup"><span data-stu-id="52774-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="52774-105">ODBCTranslator 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="52774-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="52774-106">Column</span><span class="sxs-lookup"><span data-stu-id="52774-106">Column</span></span>      | <span data-ttu-id="52774-107">類型</span><span class="sxs-lookup"><span data-stu-id="52774-107">Type</span></span>                         | <span data-ttu-id="52774-108">答案</span><span class="sxs-lookup"><span data-stu-id="52774-108">Key</span></span> | <span data-ttu-id="52774-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="52774-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="52774-110">Translator</span><span class="sxs-lookup"><span data-stu-id="52774-110">Translator</span></span>  | [<span data-ttu-id="52774-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="52774-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="52774-112">Y</span><span class="sxs-lookup"><span data-stu-id="52774-112">Y</span></span>   | <span data-ttu-id="52774-113">N</span><span class="sxs-lookup"><span data-stu-id="52774-113">N</span></span>        |
| <span data-ttu-id="52774-114">元件\_</span><span class="sxs-lookup"><span data-stu-id="52774-114">Component\_</span></span> | [<span data-ttu-id="52774-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="52774-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="52774-116">N</span><span class="sxs-lookup"><span data-stu-id="52774-116">N</span></span>   | <span data-ttu-id="52774-117">N</span><span class="sxs-lookup"><span data-stu-id="52774-117">N</span></span>        |
| <span data-ttu-id="52774-118">Description</span><span class="sxs-lookup"><span data-stu-id="52774-118">Description</span></span> | [<span data-ttu-id="52774-119">Text</span><span class="sxs-lookup"><span data-stu-id="52774-119">Text</span></span>](text.md)             | <span data-ttu-id="52774-120">N</span><span class="sxs-lookup"><span data-stu-id="52774-120">N</span></span>   | <span data-ttu-id="52774-121">N</span><span class="sxs-lookup"><span data-stu-id="52774-121">N</span></span>        |
| <span data-ttu-id="52774-122">檔案\_</span><span class="sxs-lookup"><span data-stu-id="52774-122">File\_</span></span>      | [<span data-ttu-id="52774-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="52774-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="52774-124">N</span><span class="sxs-lookup"><span data-stu-id="52774-124">N</span></span>   | <span data-ttu-id="52774-125">N</span><span class="sxs-lookup"><span data-stu-id="52774-125">N</span></span>        |
| <span data-ttu-id="52774-126">檔案 \_ 設定</span><span class="sxs-lookup"><span data-stu-id="52774-126">File\_Setup</span></span> | [<span data-ttu-id="52774-127">識別碼</span><span class="sxs-lookup"><span data-stu-id="52774-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="52774-128">N</span><span class="sxs-lookup"><span data-stu-id="52774-128">N</span></span>   | <span data-ttu-id="52774-129">Y</span><span class="sxs-lookup"><span data-stu-id="52774-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="52774-130">資料行</span><span class="sxs-lookup"><span data-stu-id="52774-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="52774-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>線上翻譯</span><span class="sxs-lookup"><span data-stu-id="52774-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="52774-132">Translator 的內部權杖名稱。</span><span class="sxs-lookup"><span data-stu-id="52774-132">Internal token name for translator.</span></span> <span data-ttu-id="52774-133">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="52774-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="52774-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="52774-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="52774-135">元件資料表中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="52774-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="52774-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="52774-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="52774-137">針對此 ODBC 驅動程式轉譯器註冊的描述。</span><span class="sxs-lookup"><span data-stu-id="52774-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="52774-138">此值無法當地語系化。</span><span class="sxs-lookup"><span data-stu-id="52774-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="52774-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="52774-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="52774-140">轉譯器資料行中所列的傳送之 DLL 檔。</span><span class="sxs-lookup"><span data-stu-id="52774-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="52774-141">File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="52774-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="52774-142">在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。</span><span class="sxs-lookup"><span data-stu-id="52774-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="52774-143">\|無法使用 SFN LFN 語法。</span><span class="sxs-lookup"><span data-stu-id="52774-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="52774-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>檔案 \_ 設定</span><span class="sxs-lookup"><span data-stu-id="52774-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="52774-145">Translator 的安裝程式 DLL 檔（如果它與 Translator 資料行不同）。</span><span class="sxs-lookup"><span data-stu-id="52774-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="52774-146">File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="52774-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="52774-147">在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。</span><span class="sxs-lookup"><span data-stu-id="52774-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="52774-148">\|無法使用 SFN LFN 語法。</span><span class="sxs-lookup"><span data-stu-id="52774-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52774-149">備註</span><span class="sxs-lookup"><span data-stu-id="52774-149">Remarks</span></span>

<span data-ttu-id="52774-150">[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="52774-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="52774-151">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="52774-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="52774-152">驗證</span><span class="sxs-lookup"><span data-stu-id="52774-152">Validation</span></span>

<dl>

[<span data-ttu-id="52774-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="52774-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="52774-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="52774-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="52774-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="52774-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



