---
description: SetODBCFolders 動作會檢查系統上是否有現有的 ODBC 驅動程式，並將每個新驅動程式的目標目錄設定為現有驅動程式的位置。
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: SetODBCFolders 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970374"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="931c9-103">SetODBCFolders 動作</span><span class="sxs-lookup"><span data-stu-id="931c9-103">SetODBCFolders Action</span></span>

<span data-ttu-id="931c9-104">SetODBCFolders 動作會檢查系統上是否有現有的 ODBC 驅動程式，並將每個新驅動程式的目標目錄設定為現有驅動程式的位置。</span><span class="sxs-lookup"><span data-stu-id="931c9-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="931c9-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="931c9-105">Sequence Restrictions</span></span>

<span data-ttu-id="931c9-106">SetODBCFolders 動作必須在 [CostFinalize 動作](costfinalize-action.md) 之後，以及在 [InstallValidate 動作](installvalidate-action.md)之前。</span><span class="sxs-lookup"><span data-stu-id="931c9-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="931c9-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="931c9-107">ActionData Messages</span></span>



| <span data-ttu-id="931c9-108">欄位</span><span class="sxs-lookup"><span data-stu-id="931c9-108">Field</span></span> | <span data-ttu-id="931c9-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="931c9-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="931c9-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="931c9-110">\[1\]</span></span> | <span data-ttu-id="931c9-111">驅動程式描述。</span><span class="sxs-lookup"><span data-stu-id="931c9-111">Driver description.</span></span> <span data-ttu-id="931c9-112">ODBC 驅動程式金鑰。</span><span class="sxs-lookup"><span data-stu-id="931c9-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="931c9-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="931c9-113">\[2\]</span></span> | <span data-ttu-id="931c9-114">新驅動程式的原始檔案夾位置。</span><span class="sxs-lookup"><span data-stu-id="931c9-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="931c9-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="931c9-115">\[3\]</span></span> | <span data-ttu-id="931c9-116">新驅動程式的新資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="931c9-116">New folder location for the new driver.</span></span> <span data-ttu-id="931c9-117">這是現有驅動程式的位置。</span><span class="sxs-lookup"><span data-stu-id="931c9-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="931c9-118">備註</span><span class="sxs-lookup"><span data-stu-id="931c9-118">Remarks</span></span>

<span data-ttu-id="931c9-119">此動作會將新的驅動程式放入與要取代之現有驅動程式相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="931c9-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="931c9-120">SetODBCFolders 動作會使用 [目錄資料表](directory-table.md) 來設定即將取代之現有驅動程式的位置。</span><span class="sxs-lookup"><span data-stu-id="931c9-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



