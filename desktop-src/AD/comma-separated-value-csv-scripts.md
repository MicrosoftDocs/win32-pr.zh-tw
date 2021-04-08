---
title: 逗點分隔值 (CSV) 腳本
description: Windows 2000 包含命令列公用程式 CSVDE，可使用 .csv 檔案匯入目錄物件，並將目錄物件匯出為 .csv 檔案。
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- 逗點分隔值腳本廣告
- 腳本，逗點分隔值 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671000"
---
# <a name="comma-separated-value-csv-scripts"></a><span data-ttu-id="a3245-105">逗點分隔值 (CSV) 腳本</span><span class="sxs-lookup"><span data-stu-id="a3245-105">Comma-separated Value (CSV) Scripts</span></span>

<span data-ttu-id="a3245-106">Windows 2000 包含命令列公用程式 CSVDE，可使用 .csv 檔案匯入目錄物件，並將目錄物件匯出為 .csv 檔案。</span><span class="sxs-lookup"><span data-stu-id="a3245-106">Windows 2000 includes a command-line utility, CSVDE, to import directory objects using .csv files and export directory objects as .csv files.</span></span> <span data-ttu-id="a3245-107">系統會建立 CSV 腳本以方便使用。</span><span class="sxs-lookup"><span data-stu-id="a3245-107">CSV scripts are created for ease-of-use.</span></span> <span data-ttu-id="a3245-108">腳本中的第一行會識別接下來各行中的屬性。</span><span class="sxs-lookup"><span data-stu-id="a3245-108">The first line in the script identifies the attributes in the lines that follow.</span></span> <span data-ttu-id="a3245-109">資料行是以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="a3245-109">Columns are separated by commas.</span></span> <span data-ttu-id="a3245-110">檔案格式與 Microsoft Excel .csv 格式相容，因此可以輕鬆地建立檔案。</span><span class="sxs-lookup"><span data-stu-id="a3245-110">The file format is compatible with the Microsoft Excel .csv format, so that files are easily created.</span></span> <span data-ttu-id="a3245-111">使用 Excel 或任何其他可以讀取和寫入 .csv 檔案的工具。</span><span class="sxs-lookup"><span data-stu-id="a3245-111">Use Excel or any other tool that can read and write .csv files.</span></span> <span data-ttu-id="a3245-112">CSVDE 支援 Unicode。</span><span class="sxs-lookup"><span data-stu-id="a3245-112">CSVDE supports Unicode.</span></span>

## <a name="example-csv-file"></a><span data-ttu-id="a3245-113">範例 CSV 檔案</span><span class="sxs-lookup"><span data-stu-id="a3245-113">Example CSV File</span></span>

<span data-ttu-id="a3245-114">下列程式碼範例是新增輔助類別的 CSV 檔案。</span><span class="sxs-lookup"><span data-stu-id="a3245-114">The following code example is a CSV file that adds an auxiliary class.</span></span>

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




