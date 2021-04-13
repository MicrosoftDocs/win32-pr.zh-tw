---
description: '[流覽] 對話方塊可讓使用者選取目錄。 目錄不一定要存在，而且可以使用此控制項來建立。'
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: 流覽對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386199"
---
# <a name="browse-dialog"></a><span data-ttu-id="9d69f-104">流覽對話方塊</span><span class="sxs-lookup"><span data-stu-id="9d69f-104">Browse Dialog</span></span>

<span data-ttu-id="9d69f-105">[流覽] 對話方塊可讓使用者選取目錄。</span><span class="sxs-lookup"><span data-stu-id="9d69f-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="9d69f-106">目錄不一定要存在，而且可以使用此控制項來建立。</span><span class="sxs-lookup"><span data-stu-id="9d69f-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="9d69f-107">這種類型的對話方塊通常包含下列三個控制項。</span><span class="sxs-lookup"><span data-stu-id="9d69f-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="9d69f-108">這些控制項會連接至相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="9d69f-108">These controls are connected to the same property.</span></span> <span data-ttu-id="9d69f-109">該屬性是要選取的路徑。</span><span class="sxs-lookup"><span data-stu-id="9d69f-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="9d69f-110">[PathEdit 控制項](pathedit-control.md)，可選取路徑的 tail 區段。</span><span class="sxs-lookup"><span data-stu-id="9d69f-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="9d69f-111">如果輸入的尾在目前磁片區上無效，則此控制項不會遺失焦點。</span><span class="sxs-lookup"><span data-stu-id="9d69f-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="9d69f-112">[DirectoryCombo 控制項](directorycombo-control.md)，可顯示 PathEdit 控制項所顯示之目前選取的路徑。</span><span class="sxs-lookup"><span data-stu-id="9d69f-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="9d69f-113">此控制項不會顯示路徑的最後一個區段。</span><span class="sxs-lookup"><span data-stu-id="9d69f-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="9d69f-114">[DirectoryList 控制項](directorylist-control.md)，可顯示 DirectoryCombo 目前所顯示之目錄底下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9d69f-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="9d69f-115">這也可能會顯示尚未建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9d69f-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="9d69f-116">[流覽] 對話方塊通常也包含 [DirectoryCombo 控制項](directorycombo-control.md) ，可指定要顯示的磁片區類型。</span><span class="sxs-lookup"><span data-stu-id="9d69f-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="9d69f-117">在 [流覽] 對話方塊上顯示的所有磁片區類型都很常見。</span><span class="sxs-lookup"><span data-stu-id="9d69f-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="9d69f-118">流覽對話方塊通常包含三個 [按鈕控制項](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="9d69f-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="9d69f-119">這些按鈕會連結至 [ControlEvent 資料表](controlevent-table.md)中各自的事件。</span><span class="sxs-lookup"><span data-stu-id="9d69f-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="9d69f-120">這些按鈕可用來啟用下列控制項選項。</span><span class="sxs-lookup"><span data-stu-id="9d69f-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="9d69f-121">Control 選項</span><span class="sxs-lookup"><span data-stu-id="9d69f-121">Control option</span></span> | <span data-ttu-id="9d69f-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="9d69f-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="9d69f-123">移到上一層</span><span class="sxs-lookup"><span data-stu-id="9d69f-123">Up One Level</span></span>   | [<span data-ttu-id="9d69f-124">DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="9d69f-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="9d69f-125">新增資料夾</span><span class="sxs-lookup"><span data-stu-id="9d69f-125">New Folder</span></span>     | [<span data-ttu-id="9d69f-126">DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="9d69f-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="9d69f-127">開啟</span><span class="sxs-lookup"><span data-stu-id="9d69f-127">Open</span></span>           | [<span data-ttu-id="9d69f-128">DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="9d69f-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="9d69f-129">若要讓 [新增資料夾] 選項使用非預設的資料夾名稱，必須在 [UIText 資料表](uitext-table.md)中指定新資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="9d69f-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="9d69f-130">路徑字串應該使用「簡短檔案名 \| 長檔名」形式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9d69f-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="9d69f-131">例如，使用 "MyProd ~ 1 \| My Fabulous Product" 之類的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9d69f-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="9d69f-132">如需檔案名格式的詳細資訊，請參閱 [Filename](filename.md) 資料行資料類型。</span><span class="sxs-lookup"><span data-stu-id="9d69f-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="9d69f-133">如果路徑不存在於 UIText 資料表中，或設定為無效值，則預設會將它設定為 "Fldr \| New Folder" 值。</span><span class="sxs-lookup"><span data-stu-id="9d69f-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="9d69f-134">如果對話方塊只需要搜尋現有的資料夾，就可以省略 [ **新增資料夾** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9d69f-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



