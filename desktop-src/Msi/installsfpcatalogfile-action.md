---
description: InstallSFPCatalogFile 動作會安裝 Windows Me 用於 Windows 檔案保護的目錄。
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: InstallSFPCatalogFile 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971177"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="81fa0-103">InstallSFPCatalogFile 動作</span><span class="sxs-lookup"><span data-stu-id="81fa0-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="81fa0-104">InstallSFPCatalogFile 動作會安裝 Windows Me 用於 Windows 檔案保護的目錄。</span><span class="sxs-lookup"><span data-stu-id="81fa0-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="81fa0-105">InstallSFPCatalogFile 會查詢 [Component 資料表](component-table.md)、 [File table](file-table.md)、 [FileSFPCatalog table](filesfpcatalog-table.md) 和 [SFPCatalog 資料表](sfpcatalog-table.md)。</span><span class="sxs-lookup"><span data-stu-id="81fa0-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="81fa0-106">如果目錄與元件中針對本機安裝所設定的檔案相關聯，或是與在本機安裝的元件中修復的檔案相關聯，就會安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="81fa0-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="81fa0-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="81fa0-107">Sequence Restrictions</span></span>

<span data-ttu-id="81fa0-108">InstallSFPCatalogFile 動作必須在 [InstallFiles](installfiles-action.md) 之前和 [CostFinalize](costfinalize-action.md)之後排序。</span><span class="sxs-lookup"><span data-stu-id="81fa0-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="81fa0-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="81fa0-109">ActionData Messages</span></span>



| <span data-ttu-id="81fa0-110">欄位</span><span class="sxs-lookup"><span data-stu-id="81fa0-110">Field</span></span> | <span data-ttu-id="81fa0-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="81fa0-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="81fa0-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="81fa0-112">\[1\]</span></span> | <span data-ttu-id="81fa0-113">要安裝的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="81fa0-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="81fa0-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="81fa0-114">\[2\]</span></span> | <span data-ttu-id="81fa0-115">此目錄安裝所依據的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="81fa0-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="81fa0-116">備註</span><span class="sxs-lookup"><span data-stu-id="81fa0-116">Remarks</span></span>

<span data-ttu-id="81fa0-117">相依于在父類別目錄之後安裝之其他目錄的目錄。</span><span class="sxs-lookup"><span data-stu-id="81fa0-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



