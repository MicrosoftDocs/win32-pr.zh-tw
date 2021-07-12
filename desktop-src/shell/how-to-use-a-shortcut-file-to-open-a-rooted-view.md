---
description: 您可以透過快捷方式檔案，將連接點的根目錄檢視啟動至該連接點。
title: 如何透過快捷方式檔案開啟連接點的根目錄檢視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581606"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="d3c8a-103">如何透過快捷方式檔案開啟連接點的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="d3c8a-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="d3c8a-104">您可以透過 [快捷方式](./links.md) 檔案，將連接點的根目錄檢視啟動至該連接點。</span><span class="sxs-lookup"><span data-stu-id="d3c8a-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="d3c8a-105">指示</span><span class="sxs-lookup"><span data-stu-id="d3c8a-105">Instructions</span></span>


<span data-ttu-id="d3c8a-106">使用/root 旗標，將快捷方式檔案的目標行設定為 Explorer.exe。</span><span class="sxs-lookup"><span data-stu-id="d3c8a-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="d3c8a-107">命令的確切形式取決於連接點的位置：</span><span class="sxs-lookup"><span data-stu-id="d3c8a-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="d3c8a-108">如果連接點是桌面的子資料夾，請使用：</span><span class="sxs-lookup"><span data-stu-id="d3c8a-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="d3c8a-109">如果連接點是檔系統資料夾，請使用：</span><span class="sxs-lookup"><span data-stu-id="d3c8a-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="d3c8a-110">如果連接點是系統虛擬資料夾的子資料夾，請使用：</span><span class="sxs-lookup"><span data-stu-id="d3c8a-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="d3c8a-111">可以包含連接點的系統虛擬資料夾具有下列類別識別碼 (Clsid) ：</span><span class="sxs-lookup"><span data-stu-id="d3c8a-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    | <span data-ttu-id="d3c8a-112">系統資料夾</span><span class="sxs-lookup"><span data-stu-id="d3c8a-112">System folder</span></span>     | <span data-ttu-id="d3c8a-113">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="d3c8a-113">Class identifier</span></span>                       |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="d3c8a-114">我的電腦</span><span class="sxs-lookup"><span data-stu-id="d3c8a-114">My Computer</span></span>       | <span data-ttu-id="d3c8a-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="d3c8a-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="d3c8a-116">網路上的芳鄰</span><span class="sxs-lookup"><span data-stu-id="d3c8a-116">My Network Places</span></span> | <span data-ttu-id="d3c8a-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="d3c8a-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="d3c8a-118">控制台</span><span class="sxs-lookup"><span data-stu-id="d3c8a-118">Control Panel</span></span>     | <span data-ttu-id="d3c8a-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="d3c8a-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="d3c8a-120">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="d3c8a-120">Internet Explorer</span></span> | <span data-ttu-id="d3c8a-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="d3c8a-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="d3c8a-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3c8a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3c8a-123">指定命名空間延伸模組的位置</span><span class="sxs-lookup"><span data-stu-id="d3c8a-123">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="d3c8a-124">如何透過登錄開啟連接點的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="d3c8a-124">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 
