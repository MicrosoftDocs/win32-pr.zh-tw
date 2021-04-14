---
description: ODBCDriver 資料表會列出屬於安裝的 ODBC 驅動程式。
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: ODBCDriver 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511189"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="d8a4d-103">ODBCDriver 資料表</span><span class="sxs-lookup"><span data-stu-id="d8a4d-103">ODBCDriver Table</span></span>

<span data-ttu-id="d8a4d-104">ODBCDriver 資料表會列出屬於安裝的 ODBC 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="d8a4d-105">ODBCDriver 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="d8a4d-106">Column</span><span class="sxs-lookup"><span data-stu-id="d8a4d-106">Column</span></span>      | <span data-ttu-id="d8a4d-107">類型</span><span class="sxs-lookup"><span data-stu-id="d8a4d-107">Type</span></span>                         | <span data-ttu-id="d8a4d-108">答案</span><span class="sxs-lookup"><span data-stu-id="d8a4d-108">Key</span></span> | <span data-ttu-id="d8a4d-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d8a4d-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d8a4d-110">驅動程式</span><span class="sxs-lookup"><span data-stu-id="d8a4d-110">Driver</span></span>      | [<span data-ttu-id="d8a4d-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="d8a4d-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8a4d-112">Y</span><span class="sxs-lookup"><span data-stu-id="d8a4d-112">Y</span></span>   | <span data-ttu-id="d8a4d-113">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-113">N</span></span>        |
| <span data-ttu-id="d8a4d-114">元件\_</span><span class="sxs-lookup"><span data-stu-id="d8a4d-114">Component\_</span></span> | [<span data-ttu-id="d8a4d-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="d8a4d-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8a4d-116">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-116">N</span></span>   | <span data-ttu-id="d8a4d-117">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-117">N</span></span>        |
| <span data-ttu-id="d8a4d-118">Description</span><span class="sxs-lookup"><span data-stu-id="d8a4d-118">Description</span></span> | [<span data-ttu-id="d8a4d-119">Text</span><span class="sxs-lookup"><span data-stu-id="d8a4d-119">Text</span></span>](text.md)             | <span data-ttu-id="d8a4d-120">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-120">N</span></span>   | <span data-ttu-id="d8a4d-121">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-121">N</span></span>        |
| <span data-ttu-id="d8a4d-122">檔案\_</span><span class="sxs-lookup"><span data-stu-id="d8a4d-122">File\_</span></span>      | [<span data-ttu-id="d8a4d-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="d8a4d-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8a4d-124">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-124">N</span></span>   | <span data-ttu-id="d8a4d-125">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-125">N</span></span>        |
| <span data-ttu-id="d8a4d-126">檔案 \_ 設定</span><span class="sxs-lookup"><span data-stu-id="d8a4d-126">File\_Setup</span></span> | [<span data-ttu-id="d8a4d-127">識別碼</span><span class="sxs-lookup"><span data-stu-id="d8a4d-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8a4d-128">N</span><span class="sxs-lookup"><span data-stu-id="d8a4d-128">N</span></span>   | <span data-ttu-id="d8a4d-129">Y</span><span class="sxs-lookup"><span data-stu-id="d8a4d-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d8a4d-130">資料行</span><span class="sxs-lookup"><span data-stu-id="d8a4d-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d8a4d-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>司機</span><span class="sxs-lookup"><span data-stu-id="d8a4d-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="d8a4d-132">驅動程式的內部權杖名稱。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-132">Internal token name for driver.</span></span> <span data-ttu-id="d8a4d-133">資料表的主鍵</span><span class="sxs-lookup"><span data-stu-id="d8a4d-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="d8a4d-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="d8a4d-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d8a4d-135">元件資料表中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="d8a4d-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="d8a4d-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="d8a4d-137">為此 ODBC 驅動程式註冊的描述。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="d8a4d-138">此值無法當地語系化。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="d8a4d-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_</span><span class="sxs-lookup"><span data-stu-id="d8a4d-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="d8a4d-140">驅動程式資料行中所列之驅動程式的 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="d8a4d-141">File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="d8a4d-142">在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="d8a4d-143">\|無法使用 SFN LFN 語法。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="d8a4d-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>檔案 \_ 設定</span><span class="sxs-lookup"><span data-stu-id="d8a4d-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="d8a4d-145">如果驅動程式與驅動程式不同，則為驅動程式的安裝程式 DLL 檔。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="d8a4d-146">File 資料 \_ 行是檔案 [資料表](file-table.md)中的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="d8a4d-147">在該檔資料表記錄的 Filename 資料行中輸入的檔案名必須是簡短的檔案名格式。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="d8a4d-148">\|無法使用 SFN LFN 語法。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8a4d-149">備註</span><span class="sxs-lookup"><span data-stu-id="d8a4d-149">Remarks</span></span>

<span data-ttu-id="d8a4d-150">[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="d8a4d-151">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="d8a4d-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="d8a4d-152">驗證</span><span class="sxs-lookup"><span data-stu-id="d8a4d-152">Validation</span></span>

<dl>

[<span data-ttu-id="d8a4d-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="d8a4d-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d8a4d-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="d8a4d-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d8a4d-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="d8a4d-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



