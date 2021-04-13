---
description: 由於現有的應用程式已過期或不再使用，因此您可能需要移除它們。
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: 刪除 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385960"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="8feb0-103">刪除 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="8feb0-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="8feb0-104">由於現有的應用程式已過期或不再使用，因此您可能需要移除它們。</span><span class="sxs-lookup"><span data-stu-id="8feb0-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="8feb0-105">**若要刪除 COM + 應用程式**</span><span class="sxs-lookup"><span data-stu-id="8feb0-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="8feb0-106">在 [元件服務] 系統管理工具的主控台樹中，選取您要刪除應用程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="8feb0-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="8feb0-107">開啟指定電腦的 [ **Com + 應用程式** ] 資料夾，以顯示所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8feb0-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="8feb0-108">選取您要移除的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8feb0-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="8feb0-109">如果您是選取伺服器應用程式，請關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="8feb0-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="8feb0-110">您可以在 [元件服務] 系統管理工具中選取應用程式，以滑鼠右鍵按一下，然後按一下 [ **關機**]，以關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="8feb0-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="8feb0-111">如果您選取了程式庫應用程式，請確定目前使用此程式庫應用程式的所有進程都已關閉。</span><span class="sxs-lookup"><span data-stu-id="8feb0-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="8feb0-112">在 [ **動作** ] 功能表上，按一下 [ **刪除**]。</span><span class="sxs-lookup"><span data-stu-id="8feb0-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="8feb0-113">您也可以用滑鼠右鍵按一下應用程式名稱，然後按一下 [ **刪除**]。</span><span class="sxs-lookup"><span data-stu-id="8feb0-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="8feb0-114">您也可以在 [元件服務] 系統管理工具中選取應用程式，然後按下 **delete** 鍵，也可以選取應用程式、按一下滑鼠右鍵，然後按一下 [ **刪除**]，以刪除應用程式。</span><span class="sxs-lookup"><span data-stu-id="8feb0-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="8feb0-115">當系統提示您確認您的動作時，請按一下 **[是]** 。</span><span class="sxs-lookup"><span data-stu-id="8feb0-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="8feb0-116">此外，如果使用 Windows Installer (的電腦上安裝了伺服器應用程式或應用程式 proxy （如 < 安裝 COM + 應用程式) 中所述），您可以在 Microsoft Windows 主控台中透過 [新增/移除程式] 公用程式來刪除它。</span><span class="sxs-lookup"><span data-stu-id="8feb0-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="8feb0-117">或者，您可以使用 Windows Installer 命令列語法來刪除已安裝的伺服器應用程式或應用程式 proxy：</span><span class="sxs-lookup"><span data-stu-id="8feb0-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="8feb0-118">**msiexec-x** *應用程式 \_ 名稱 \* \* \* .msi*\*</span><span class="sxs-lookup"><span data-stu-id="8feb0-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="8feb0-119">這些方法特別適用于在未執行「元件服務」系統管理工具的用戶端電腦上刪除 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8feb0-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="8feb0-120">刪除應用程式也會刪除應用程式中包含的任何元件。</span><span class="sxs-lookup"><span data-stu-id="8feb0-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="8feb0-121">如果這些元件相依于其他資源 (資料庫連線、資料或文字檔、IIS 虛擬根目錄設定等等) ，則必須透過 [元件服務] 系統管理工具以外的機制移除這些資源。</span><span class="sxs-lookup"><span data-stu-id="8feb0-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8feb0-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="8feb0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8feb0-123">複製元件</span><span class="sxs-lookup"><span data-stu-id="8feb0-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="8feb0-124">建立新的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="8feb0-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="8feb0-125">匯入元件</span><span class="sxs-lookup"><span data-stu-id="8feb0-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="8feb0-126">安裝新元件</span><span class="sxs-lookup"><span data-stu-id="8feb0-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="8feb0-127">移動元件</span><span class="sxs-lookup"><span data-stu-id="8feb0-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="8feb0-128">從 COM + 應用程式移除元件</span><span class="sxs-lookup"><span data-stu-id="8feb0-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



