---
description: ODBCDataSource 資料表會列出屬於安裝的資料來源。
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: ODBCDataSource 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973498"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="9fc03-103">ODBCDataSource 資料表</span><span class="sxs-lookup"><span data-stu-id="9fc03-103">ODBCDataSource Table</span></span>

<span data-ttu-id="9fc03-104">ODBCDataSource 資料表會列出屬於安裝的資料來源。</span><span class="sxs-lookup"><span data-stu-id="9fc03-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="9fc03-105">ODBCDataSource 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="9fc03-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="9fc03-106">Column</span><span class="sxs-lookup"><span data-stu-id="9fc03-106">Column</span></span>            | <span data-ttu-id="9fc03-107">類型</span><span class="sxs-lookup"><span data-stu-id="9fc03-107">Type</span></span>                         | <span data-ttu-id="9fc03-108">答案</span><span class="sxs-lookup"><span data-stu-id="9fc03-108">Key</span></span> | <span data-ttu-id="9fc03-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="9fc03-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="9fc03-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="9fc03-110">DataSource</span></span>        | [<span data-ttu-id="9fc03-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="9fc03-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="9fc03-112">Y</span><span class="sxs-lookup"><span data-stu-id="9fc03-112">Y</span></span>   | <span data-ttu-id="9fc03-113">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-113">N</span></span>        |
| <span data-ttu-id="9fc03-114">元件\_</span><span class="sxs-lookup"><span data-stu-id="9fc03-114">Component\_</span></span>       | [<span data-ttu-id="9fc03-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="9fc03-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="9fc03-116">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-116">N</span></span>   | <span data-ttu-id="9fc03-117">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-117">N</span></span>        |
| <span data-ttu-id="9fc03-118">Description</span><span class="sxs-lookup"><span data-stu-id="9fc03-118">Description</span></span>       | [<span data-ttu-id="9fc03-119">Text</span><span class="sxs-lookup"><span data-stu-id="9fc03-119">Text</span></span>](text.md)             | <span data-ttu-id="9fc03-120">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-120">N</span></span>   | <span data-ttu-id="9fc03-121">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-121">N</span></span>        |
| <span data-ttu-id="9fc03-122">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="9fc03-122">DriverDescription</span></span> | [<span data-ttu-id="9fc03-123">Text</span><span class="sxs-lookup"><span data-stu-id="9fc03-123">Text</span></span>](text.md)             | <span data-ttu-id="9fc03-124">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-124">N</span></span>   | <span data-ttu-id="9fc03-125">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-125">N</span></span>        |
| <span data-ttu-id="9fc03-126">註冊</span><span class="sxs-lookup"><span data-stu-id="9fc03-126">Registration</span></span>      | [<span data-ttu-id="9fc03-127">整數</span><span class="sxs-lookup"><span data-stu-id="9fc03-127">Integer</span></span>](integer.md)       | <span data-ttu-id="9fc03-128">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-128">N</span></span>   | <span data-ttu-id="9fc03-129">N</span><span class="sxs-lookup"><span data-stu-id="9fc03-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9fc03-130">資料行</span><span class="sxs-lookup"><span data-stu-id="9fc03-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9fc03-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>資料來源</span><span class="sxs-lookup"><span data-stu-id="9fc03-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="9fc03-132">資料來源的內部 token 名稱。</span><span class="sxs-lookup"><span data-stu-id="9fc03-132">Internal token name for data source.</span></span> <span data-ttu-id="9fc03-133">資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="9fc03-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="9fc03-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="9fc03-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="9fc03-135">[元件資料表](component-table.md)中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9fc03-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fc03-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="9fc03-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="9fc03-137">為此資料來源註冊的描述。</span><span class="sxs-lookup"><span data-stu-id="9fc03-137">The description registered for this data source.</span></span> <span data-ttu-id="9fc03-138">此值無法當地語系化。</span><span class="sxs-lookup"><span data-stu-id="9fc03-138">This value cannot be localized.</span></span> <span data-ttu-id="9fc03-139">ODBC 資料來源描述不能超過 \_ SQL \_ \_ 的 DSN 長度上限。</span><span class="sxs-lookup"><span data-stu-id="9fc03-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="9fc03-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span><span class="sxs-lookup"><span data-stu-id="9fc03-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="9fc03-141">可能已預先存在的相關聯驅動程式。</span><span class="sxs-lookup"><span data-stu-id="9fc03-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="9fc03-142">此值無法當地語系化。</span><span class="sxs-lookup"><span data-stu-id="9fc03-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="9fc03-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>註冊</span><span class="sxs-lookup"><span data-stu-id="9fc03-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="9fc03-144">此欄位會指定資料來源的註冊類型。</span><span class="sxs-lookup"><span data-stu-id="9fc03-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="9fc03-145">常數</span><span class="sxs-lookup"><span data-stu-id="9fc03-145">Constant</span></span>                                      | <span data-ttu-id="9fc03-146">十六進位</span><span class="sxs-lookup"><span data-stu-id="9fc03-146">Hexadecimal</span></span> | <span data-ttu-id="9fc03-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="9fc03-147">Decimal</span></span> | <span data-ttu-id="9fc03-148">Description</span><span class="sxs-lookup"><span data-stu-id="9fc03-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="9fc03-149">**msidbODBCDataSourceRegistrationPerMachine**</span><span class="sxs-lookup"><span data-stu-id="9fc03-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="9fc03-150">0x000</span><span class="sxs-lookup"><span data-stu-id="9fc03-150">0x000</span></span>       | <span data-ttu-id="9fc03-151">0</span><span class="sxs-lookup"><span data-stu-id="9fc03-151">0</span></span>       | <span data-ttu-id="9fc03-152">每一部電腦都會註冊資料來源。</span><span class="sxs-lookup"><span data-stu-id="9fc03-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="9fc03-153">**msidbODBCDataSourceRegistrationPerUser**</span><span class="sxs-lookup"><span data-stu-id="9fc03-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="9fc03-154">0x001</span><span class="sxs-lookup"><span data-stu-id="9fc03-154">0x001</span></span>       | <span data-ttu-id="9fc03-155">1</span><span class="sxs-lookup"><span data-stu-id="9fc03-155">1</span></span>       | <span data-ttu-id="9fc03-156">每位使用者都會註冊資料來源。</span><span class="sxs-lookup"><span data-stu-id="9fc03-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fc03-157">備註</span><span class="sxs-lookup"><span data-stu-id="9fc03-157">Remarks</span></span>

<span data-ttu-id="9fc03-158">[*順序資料表*](s-gly.md)中的 [InstallODBC](installodbc-action.md)和 [RemoveODBC](removeodbc-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="9fc03-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="9fc03-159">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="9fc03-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="9fc03-160">驗證</span><span class="sxs-lookup"><span data-stu-id="9fc03-160">Validation</span></span>

<dl>

[<span data-ttu-id="9fc03-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="9fc03-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9fc03-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="9fc03-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9fc03-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="9fc03-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9fc03-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="9fc03-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="9fc03-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="9fc03-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



