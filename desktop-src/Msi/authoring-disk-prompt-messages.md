---
description: 您可以使用下列指導方針來撰寫 Windows Installer 安裝，此安裝程式會顯示訊息方塊，以提示使用者插入磁片。
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: 撰寫磁片提示訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989363"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="910f8-103">撰寫磁片提示訊息</span><span class="sxs-lookup"><span data-stu-id="910f8-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="910f8-104">您可以使用下列指導方針來撰寫 Windows Installer 安裝，此安裝程式會顯示訊息方塊，以提示使用者插入磁片。</span><span class="sxs-lookup"><span data-stu-id="910f8-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="910f8-105">**若要顯示訊息方塊以提示使用者插入磁片**</span><span class="sxs-lookup"><span data-stu-id="910f8-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="910f8-106">您可以使用安裝程式的撰寫功能，在 [屬性](property-table.md)表中設定 [**DiskPrompt**](diskprompt.md)屬性字串。</span><span class="sxs-lookup"><span data-stu-id="910f8-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="910f8-107">這應該包含要安裝的產品名稱，以及在磁片上列印的標題字串內的預留位置參數。</span><span class="sxs-lookup"><span data-stu-id="910f8-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="910f8-108">例如，針對 Microsoft Publisher， **DiskPrompt** 屬性可能是「Microsoft Publisher： disk \[ 1」 \] ，其中 \[ 1 \] 是磁片標題的預留位置。</span><span class="sxs-lookup"><span data-stu-id="910f8-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="910f8-109">輸入每個磁片的標題，以提示輸入 [媒體](media-table.md) 資料表中 DiskPrompt 資料行的個別資料列。</span><span class="sxs-lookup"><span data-stu-id="910f8-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="910f8-110">例如，媒體資料表中的第一個和唯一一個專案可能是「1–安裝」。</span><span class="sxs-lookup"><span data-stu-id="910f8-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="910f8-111">在 [InstallFiles](installfiles-action.md) 動作期間， [媒體](media-table.md) 資料表 DiskPrompt 資料行中的值會取代為 [**DiskPrompt**](diskprompt.md) 屬性字串中的預留位置。</span><span class="sxs-lookup"><span data-stu-id="910f8-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="910f8-112">訊息方塊所顯示的訊息是從 [錯誤資料表](error-table.md)內建的範本字串所建立。</span><span class="sxs-lookup"><span data-stu-id="910f8-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="910f8-113">這是錯誤1302，範本字串為：「請插入磁片：2」 \[ \] ，而 \[ 2 \] 代表 [**DiskPrompt**](diskprompt.md) 屬性的預留位置。</span><span class="sxs-lookup"><span data-stu-id="910f8-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="910f8-114">此範例會對使用者顯示下列訊息：「請插入磁片： Microsoft Publisher： Disk 1 – Install」。</span><span class="sxs-lookup"><span data-stu-id="910f8-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="910f8-115">請注意，除了 [無] 以外的所有 [消費者介面層級](user-interface-levels.md) ，都會顯示磁片提示訊息。</span><span class="sxs-lookup"><span data-stu-id="910f8-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



