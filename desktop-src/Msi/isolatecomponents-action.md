---
description: IsolateComponents 動作會將元件的複本安裝 (通常是共用 DLL) 至私用位置，以供特定應用程式使用， (通常是 .exe) 。
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: IsolateComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320568"
---
# <a name="isolatecomponents-action"></a><span data-ttu-id="64b71-103">IsolateComponents 動作</span><span class="sxs-lookup"><span data-stu-id="64b71-103">IsolateComponents Action</span></span>

<span data-ttu-id="64b71-104">IsolateComponents 動作會將元件的複本安裝 (通常是共用 DLL) 至私用位置，以供特定應用程式使用， (通常是 .exe) 。</span><span class="sxs-lookup"><span data-stu-id="64b71-104">The IsolateComponents action installs a copy of a component (commonly a shared DLL) into a private location for use by a specific application (typically an .exe).</span></span> <span data-ttu-id="64b71-105">這會將應用程式與元件的其他複本隔離，以安裝到電腦上的共用位置。</span><span class="sxs-lookup"><span data-stu-id="64b71-105">This isolates the application from other copies of the component that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="64b71-106">如需詳細資訊，請參閱 [獨立元件](isolated-components.md)。</span><span class="sxs-lookup"><span data-stu-id="64b71-106">For more information, see [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="64b71-107">此動作會參考 [IsolatedComponent 資料表](isolatedcomponent-table.md) 的每一筆記錄，並將 [元件共用] 欄位中所列元件的檔案 \_ 與 [元件應用程式] 欄位中所列的元件產生關聯 \_ 。</span><span class="sxs-lookup"><span data-stu-id="64b71-107">The action refers to each record of the [IsolatedComponent table](isolatedcomponent-table.md) and associates the files of the component listed in the Component\_Shared field with the component listed in the Component\_Application field.</span></span> <span data-ttu-id="64b71-108">安裝程式會將共用的元件檔案安裝 \_ 到與元件應用程式相同的目錄中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="64b71-108">The installer installs the files of Component\_Shared into the same directory as Component\_Application.</span></span> <span data-ttu-id="64b71-109">安裝程式會在此目錄中產生檔案（長度為零個位元組），為元件應用程式使用金鑰檔的簡短檔案名， \_ (通常這與 .exe) 附加的檔案名相同。</span><span class="sxs-lookup"><span data-stu-id="64b71-109">The installer generates a file in this directory, zero bytes in length, having the short filename name of the key file for Component\_Application (typically this is the same file name as the .exe) appended with .local.</span></span> <span data-ttu-id="64b71-110">IsolatedComponent 動作不會影響元件應用程式的安裝 \_ 。</span><span class="sxs-lookup"><span data-stu-id="64b71-110">The IsolatedComponent action does not affect the installation of Component\_Application.</span></span> <span data-ttu-id="64b71-111">卸載元件 \_ 應用程式也會 \_ 從目錄中移除元件共用檔案和本機檔案。</span><span class="sxs-lookup"><span data-stu-id="64b71-111">Uninstalling Component\_Application also removes the Component\_Shared files and the .local file from the directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="64b71-112">順序限制</span><span class="sxs-lookup"><span data-stu-id="64b71-112">Sequence Restrictions</span></span>

<span data-ttu-id="64b71-113">IsolateComponents 動作只能用在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="64b71-113">The IsolateComponents action can be used only in the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="64b71-114">此動作必須在 [CostInitialize 動作](costinitialize-action.md) 之後，以及 [CostFinalize 動作](costfinalize-action.md)之前。</span><span class="sxs-lookup"><span data-stu-id="64b71-114">This action must come after the [CostInitialize action](costinitialize-action.md) and before the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="64b71-115">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="64b71-115">ActionData Messages</span></span>

<span data-ttu-id="64b71-116">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="64b71-116">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b71-117">備註</span><span class="sxs-lookup"><span data-stu-id="64b71-117">Remarks</span></span>

<span data-ttu-id="64b71-118">如果 [IsolateComponents] 動作的 [條件] 資料行評估為 True，或保留空白，則安裝程式會隔離 [IsolatedComponent 資料表](isolatedcomponent-table.md)中所列的所有元件。</span><span class="sxs-lookup"><span data-stu-id="64b71-118">If the Condition column for the IsolateComponents action evaluates to True, or is left blank, the installer isolates all the components listed in the [IsolatedComponent table](isolatedcomponent-table.md).</span></span> <span data-ttu-id="64b71-119">如果 [條件] 資料行評估為 False，則安裝程式會忽略 IsolatedComponent 資料表並照常共用這些元件。</span><span class="sxs-lookup"><span data-stu-id="64b71-119">If the Condition column evaluates to False, the installer ignores the IsolatedComponent table and shares the components usual.</span></span> <span data-ttu-id="64b71-120">[**RedirectedDllSupport**](redirecteddllsupport.md)屬性可用來條件執行此動作。</span><span class="sxs-lookup"><span data-stu-id="64b71-120">The [**RedirectedDllSupport**](redirecteddllsupport.md) property may be used to condition this action.</span></span> <span data-ttu-id="64b71-121">如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="64b71-121">For more information, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

 

 



