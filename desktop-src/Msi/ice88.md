---
description: ICE88 會驗證 Windows Installer 封裝中是否存在 IniFile 資料表的 DirProperty 資料行中所參考的目錄。
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851571"
---
# <a name="ice88"></a><span data-ttu-id="f2889-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="f2889-103">ICE88</span></span>

<span data-ttu-id="f2889-104">ICE88 會驗證 Windows Installer 封裝中是否存在 [IniFile 資料表](inifile-table.md) 的 DirProperty 資料行中所參考的目錄。</span><span class="sxs-lookup"><span data-stu-id="f2889-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="f2889-105">如果 DirProperty 值不代表目錄、AppSearch 或屬性資料表中的屬性、特定的 [系統資料夾屬性](property-reference.md)，或由類型51自訂動作所設定的屬性，ICE88 就會發出警告。</span><span class="sxs-lookup"><span data-stu-id="f2889-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="f2889-106">ICE88 會掃描下列資料表和屬性。</span><span class="sxs-lookup"><span data-stu-id="f2889-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="f2889-107">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="f2889-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="f2889-108">AppSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="f2889-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="f2889-109">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="f2889-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="f2889-110">[CustomAction 資料表](customaction-table.md) ，其中自訂動作是 [自訂動作類型 51](custom-action-type-51.md)</span><span class="sxs-lookup"><span data-stu-id="f2889-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="f2889-111">**ProgramFilesFolder 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2889-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="f2889-112">**CommonFilesFolder 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2889-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="f2889-113">**SystemFolder 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2889-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="f2889-114">**ProgramFiles64Folder 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2889-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="f2889-115">**CommonFiles64Folder 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2889-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="f2889-116">**System64Folder 屬性**</span><span class="sxs-lookup"><span data-stu-id="f2889-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="f2889-117">結果</span><span class="sxs-lookup"><span data-stu-id="f2889-117">Result</span></span>

<span data-ttu-id="f2889-118">ICE88 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="f2889-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="f2889-119">ICE88 警告</span><span class="sxs-lookup"><span data-stu-id="f2889-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="f2889-120">Description</span><span class="sxs-lookup"><span data-stu-id="f2889-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2889-121">在 IniFile 資料表專案中 (IniFile =) \[ 3 \] \[ \] ：在目錄/屬性/AppSearch/CA Type51 資料表中找不到 DirProperty = 1，而且它不是其中一個安裝程式屬性。</span><span class="sxs-lookup"><span data-stu-id="f2889-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="f2889-122">ICE88 會針對 IniFile 資料表中的每一筆記錄，讀取 DirProperty 資料行中的值。</span><span class="sxs-lookup"><span data-stu-id="f2889-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="f2889-123">ICE88 會掃描 [目錄資料表](directory-table.md)、 [AppSearch 資料表](appsearch-table.md)和 [屬性工作表](property-table.md) 中的值，也會掃描安裝程式所設定的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="f2889-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="f2889-124">如果在掃描中找不到值，ICE88 會張貼此警告。</span><span class="sxs-lookup"><span data-stu-id="f2889-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f2889-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2889-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2889-126">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="f2889-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



