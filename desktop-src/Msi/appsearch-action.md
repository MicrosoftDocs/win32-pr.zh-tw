---
description: AppSearch 動作會使用檔案簽章來搜尋現有的產品版本。
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: AppSearch 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192462"
---
# <a name="appsearch-action"></a><span data-ttu-id="500d5-103">AppSearch 動作</span><span class="sxs-lookup"><span data-stu-id="500d5-103">AppSearch Action</span></span>

<span data-ttu-id="500d5-104">AppSearch 動作會使用檔案簽章來搜尋現有的產品版本。</span><span class="sxs-lookup"><span data-stu-id="500d5-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="500d5-105">AppSearch 動作可能會使用此資訊來判斷要安裝升級的位置。</span><span class="sxs-lookup"><span data-stu-id="500d5-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="500d5-106">AppSearch 動作也可以用來將屬性設為登錄或 .ini 檔案專案的現有值。</span><span class="sxs-lookup"><span data-stu-id="500d5-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="500d5-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="500d5-107">Sequence Restrictions</span></span>

<span data-ttu-id="500d5-108">AppSearch 應該撰寫在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="500d5-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="500d5-109">如果動作已在 InstallUISequence 序列中執行，則安裝程式會防止在 InstallExecuteSequence 序列中執行 AppSearch 動作。</span><span class="sxs-lookup"><span data-stu-id="500d5-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="500d5-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="500d5-110">ActionData Messages</span></span>



| <span data-ttu-id="500d5-111">欄位</span><span class="sxs-lookup"><span data-stu-id="500d5-111">Field</span></span> | <span data-ttu-id="500d5-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="500d5-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="500d5-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="500d5-113">\[1\]</span></span> | <span data-ttu-id="500d5-114">保存檔案位置的屬性。</span><span class="sxs-lookup"><span data-stu-id="500d5-114">Property holding file location.</span></span> |
| <span data-ttu-id="500d5-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="500d5-115">\[2\]</span></span> | <span data-ttu-id="500d5-116">檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="500d5-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="500d5-117">備註</span><span class="sxs-lookup"><span data-stu-id="500d5-117">Remarks</span></span>

<span data-ttu-id="500d5-118">AppSearch 動作需要簽 [章資料表出現](signature-table.md) 在安裝套件中。</span><span class="sxs-lookup"><span data-stu-id="500d5-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="500d5-119">簽章會列在簽章資料表中。</span><span class="sxs-lookup"><span data-stu-id="500d5-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="500d5-120">不在簽章資料表中的簽章代表目錄，而動作則會將屬性設定為該簽章的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="500d5-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="500d5-121">AppSearch 動作會先使用 [CompLocator](complocator-table.md) 資料表、 [RegLocator](reglocator-table.md) 資料表、 [IniLocator](inilocator-table.md) 資料表，最後是 [DrLocator](drlocator-table.md) 資料表來搜尋檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="500d5-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="500d5-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="500d5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="500d5-123">AppSearch</span><span class="sxs-lookup"><span data-stu-id="500d5-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="500d5-124">CompLocator</span><span class="sxs-lookup"><span data-stu-id="500d5-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="500d5-125">IniLocator</span><span class="sxs-lookup"><span data-stu-id="500d5-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="500d5-126">RegLocator</span><span class="sxs-lookup"><span data-stu-id="500d5-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="500d5-127">DrLocator</span><span class="sxs-lookup"><span data-stu-id="500d5-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



