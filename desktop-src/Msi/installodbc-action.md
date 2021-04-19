---
description: InstallODBC 動作會在 ODBCDriver 資料表、ODBCTranslator 資料表和 ODBCDataSource 資料表中安裝驅動程式、轉譯程式和資料來源。
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: InstallODBC 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992090"
---
# <a name="installodbc-action"></a><span data-ttu-id="2fed3-103">InstallODBC 動作</span><span class="sxs-lookup"><span data-stu-id="2fed3-103">InstallODBC Action</span></span>

<span data-ttu-id="2fed3-104">InstallODBC 動作會在 [ODBCDriver 資料表](odbcdriver-table.md)、 [ODBCTranslator 資料表](odbctranslator-table.md)和 [ODBCDataSource 資料表](odbcdatasource-table.md)中安裝驅動程式、轉譯程式和資料來源。</span><span class="sxs-lookup"><span data-stu-id="2fed3-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="2fed3-105">如果驅動程式或轉譯器已存在，則 InstallODBC 動作會進行安裝所需的 SQL 呼叫。</span><span class="sxs-lookup"><span data-stu-id="2fed3-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2fed3-106">順序限制</span><span class="sxs-lookup"><span data-stu-id="2fed3-106">Sequence Restrictions</span></span>

<span data-ttu-id="2fed3-107">InstallODBC 動作不會複製或移除檔案，而且必須在複製或移除檔案的動作之後。</span><span class="sxs-lookup"><span data-stu-id="2fed3-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="2fed3-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="2fed3-108">ActionData Messages</span></span>

<span data-ttu-id="2fed3-109">下表指出每個已安裝驅動程式的 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="2fed3-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="2fed3-110">欄位</span><span class="sxs-lookup"><span data-stu-id="2fed3-110">Field</span></span>       | <span data-ttu-id="2fed3-111">描述</span><span class="sxs-lookup"><span data-stu-id="2fed3-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2fed3-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-112">\[1\]</span></span>       | <span data-ttu-id="2fed3-113">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="2fed3-113">Driver description.</span></span> <span data-ttu-id="2fed3-114">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="2fed3-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="2fed3-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-115">\[2\]</span></span>       | <span data-ttu-id="2fed3-116">ComponentId.</span><span class="sxs-lookup"><span data-stu-id="2fed3-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="2fed3-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-117">\[3\]</span></span>       | <span data-ttu-id="2fed3-118">資料夾。</span><span class="sxs-lookup"><span data-stu-id="2fed3-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="2fed3-119">\[4、5、.。。\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-119">\[4, 5, …\]</span></span> | <span data-ttu-id="2fed3-120">來自 [ODBCAttribute](odbcattribute-table.md)的屬性和值配對。</span><span class="sxs-lookup"><span data-stu-id="2fed3-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="2fed3-121">下錶針對每個已安裝的翻譯工具，識別 ActionData 的訊息。</span><span class="sxs-lookup"><span data-stu-id="2fed3-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="2fed3-122">欄位</span><span class="sxs-lookup"><span data-stu-id="2fed3-122">Field</span></span>       | <span data-ttu-id="2fed3-123">描述</span><span class="sxs-lookup"><span data-stu-id="2fed3-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2fed3-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-124">\[1\]</span></span>       | <span data-ttu-id="2fed3-125">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="2fed3-125">Driver description.</span></span> <span data-ttu-id="2fed3-126">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="2fed3-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="2fed3-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-127">\[2\]</span></span>       | <span data-ttu-id="2fed3-128">ComponentId.</span><span class="sxs-lookup"><span data-stu-id="2fed3-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="2fed3-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-129">\[3\]</span></span>       | <span data-ttu-id="2fed3-130">資料夾。</span><span class="sxs-lookup"><span data-stu-id="2fed3-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="2fed3-131">\[4、5、.。。\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-131">\[4, 5, …\]</span></span> | <span data-ttu-id="2fed3-132">來自 [ODBCAttribute](odbcattribute-table.md)的屬性和值配對。</span><span class="sxs-lookup"><span data-stu-id="2fed3-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="2fed3-133">下表指出每個已安裝資料來源的 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="2fed3-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="2fed3-134">欄位</span><span class="sxs-lookup"><span data-stu-id="2fed3-134">Field</span></span>       | <span data-ttu-id="2fed3-135">描述</span><span class="sxs-lookup"><span data-stu-id="2fed3-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="2fed3-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-136">\[1\]</span></span>       | <span data-ttu-id="2fed3-137">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="2fed3-137">Driver description.</span></span> <span data-ttu-id="2fed3-138">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="2fed3-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="2fed3-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-139">\[2\]</span></span>       | <span data-ttu-id="2fed3-140">ComponentId.</span><span class="sxs-lookup"><span data-stu-id="2fed3-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="2fed3-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-141">\[3\]</span></span>       | <span data-ttu-id="2fed3-142">註冊： ODBC \_ 新增 \_ DSN 或 odbc \_ 新增 \_ SYS \_ DSN。</span><span class="sxs-lookup"><span data-stu-id="2fed3-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="2fed3-143">\[4、5、.。。\]</span><span class="sxs-lookup"><span data-stu-id="2fed3-143">\[4, 5, …\]</span></span> | <span data-ttu-id="2fed3-144">來自 [ODBCAttribute](odbcattribute-table.md)的屬性和值配對。</span><span class="sxs-lookup"><span data-stu-id="2fed3-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2fed3-145">備註</span><span class="sxs-lookup"><span data-stu-id="2fed3-145">Remarks</span></span>

<span data-ttu-id="2fed3-146">ODBC 驅動程式管理員必須在 Microsoft Installer 封裝中撰寫，且必須包含名為 ODBCDriverManager 的元件。</span><span class="sxs-lookup"><span data-stu-id="2fed3-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="2fed3-147">如有必要，則會安裝管理員。</span><span class="sxs-lookup"><span data-stu-id="2fed3-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="2fed3-148">若要重新命名元件，請將名為 ODBCDriverManager 的屬性設定為元件的新名稱。</span><span class="sxs-lookup"><span data-stu-id="2fed3-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="2fed3-149">如果要安裝64位 ODBC 驅動程式管理員，則攜帶該驅動程式的元件應該命名為 ODBCDriverManager64。</span><span class="sxs-lookup"><span data-stu-id="2fed3-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="2fed3-150">InstallODBC 動作會查詢 [ODBCDataSource 資料表](odbcdatasource-table.md) 和 [ODBCSourceAttribute 資料表](odbcsourceattribute-table.md) ，找出要安裝的每個資料來源，以及資料來源的屬性。</span><span class="sxs-lookup"><span data-stu-id="2fed3-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="2fed3-151">InstallODBC 動作會針對已選取要安裝的每個驅動程式和翻譯工具，查詢 [ODBCDriver 資料表](odbcdriver-table.md) 和 [ODBCTranslator 資料表](odbctranslator-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="2fed3-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="2fed3-152">InstallODBC 動作會查詢 [ODBCAttribute 資料表](odbcattribute-table.md) ，以取得驅動程式和轉譯程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="2fed3-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fed3-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fed3-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fed3-154">Windows Installer 範例</span><span class="sxs-lookup"><span data-stu-id="2fed3-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



