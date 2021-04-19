---
description: ICE18 會驗證用來作為元件之索引鍵路徑的任何空白目錄都列在 CreateFolder 資料表中。
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992006"
---
# <a name="ice18"></a><span data-ttu-id="6ea9c-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="6ea9c-103">ICE18</span></span>

<span data-ttu-id="6ea9c-104">ICE18 會驗證用來作為元件之索引鍵路徑的任何空白目錄都列在 [CreateFolder 資料表](createfolder-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="6ea9c-105">如果 [元件資料表](component-table.md) 的 KeyPath 資料行是 Null，這表示目錄資料行中所列的目錄 \_ 是該元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="6ea9c-106">因為安裝程式所建立的資料夾是空的，所以當它變成空白時，此資料夾必須列在 [CreateFolder 表格](createfolder-table.md) 中，以防止安裝程式每次都嘗試安裝。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="6ea9c-107">請勿使 SystemFolder 目錄成為元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="6ea9c-108">因為每個作業系統上都有這個資料夾，所以安裝程式一律會偵測到元件是否存在的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="6ea9c-109">在此情況下，金鑰路徑應該是檔案、登錄專案或 ODBC 資料來源。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="6ea9c-110">執行驗證 ICE18 時，會先檢查下列條件是否成立：</span><span class="sxs-lookup"><span data-stu-id="6ea9c-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="6ea9c-111">[元件資料表](component-table.md)的 KeyPath 資料行包含 Null 值。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="6ea9c-112">檔案 [資料表](file-table.md)中沒有列出元件的檔案。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="6ea9c-113">[RemoveFile 資料表](removefile-table.md)中沒有列出元件的檔案，而且 DirProperty 中的值與 \_ [元件資料表](component-table.md)的目錄資料行相同。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="6ea9c-114">[DuplicateFile 資料表](duplicatefile-table.md)中沒有列出元件的檔案，而且 DestFolder 中的值與 \_ [元件資料表](component-table.md)的目錄資料行相同。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="6ea9c-115">[MoveFile 資料表](movefile-table.md)中沒有列出元件的檔案，而且 DestFolder 中的值與 \_ [元件資料表](component-table.md)的目錄資料行相同。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="6ea9c-116">如果這些都是 true，則 ICE18 會驗證下列各項：</span><span class="sxs-lookup"><span data-stu-id="6ea9c-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="6ea9c-117">\_ [CreateFolder 資料表](createfolder-table.md)的 component 資料行與[component 資料表](component-table.md)的 component 資料行具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="6ea9c-118">CreateFolder 資料表的目錄資料 \_ 行與 \_ [Component 資料表](component-table.md)的目錄資料行具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="6ea9c-119">結果</span><span class="sxs-lookup"><span data-stu-id="6ea9c-119">Result</span></span>

<span data-ttu-id="6ea9c-120">如果安裝套件將目錄指定為未列于 [CreateFolder 資料表](createfolder-table.md)中之元件的金鑰路徑，ICE18 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6ea9c-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ea9c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ea9c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ea9c-122">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="6ea9c-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



