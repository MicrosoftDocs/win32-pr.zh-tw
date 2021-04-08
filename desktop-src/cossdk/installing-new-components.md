---
description: 若要將元件加入至 COM + 應用程式的 [元件] 資料夾，您可以使用 [COM + 元件安裝精靈] 或從 Windows 檔案總管中包含元件的 .dll 檔案，並將它們放在應用程式中。
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: 安裝新元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025956"
---
# <a name="installing-new-components"></a><span data-ttu-id="d825b-103">安裝新元件</span><span class="sxs-lookup"><span data-stu-id="d825b-103">Installing New Components</span></span>

<span data-ttu-id="d825b-104">若要將元件加入至 COM + 應用程式的 [ **元件** ] 資料夾，您可以使用 [Com + 元件安裝精靈] 或從 Windows 檔案總管中包含元件的 .dll 檔案，並將它們放在應用程式中。</span><span class="sxs-lookup"><span data-stu-id="d825b-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="d825b-105">如果您使用 COM + 元件安裝精靈，您可以安裝新的元件，以在電腦上註冊元件，或匯入已註冊的元件。</span><span class="sxs-lookup"><span data-stu-id="d825b-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="d825b-106">元件可以新增至空的應用程式或現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d825b-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="d825b-107">**若要將元件加入至 COM + 應用程式**</span><span class="sxs-lookup"><span data-stu-id="d825b-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="d825b-108">在 [元件服務] 系統管理工具的主控台樹中，選取裝載 COM + 應用程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="d825b-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="d825b-109">開啟該電腦的 [ **Com + 應用程式** ] 資料夾，然後選取您要在其中安裝元件 (s) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d825b-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="d825b-110">開啟應用程式資料夾，然後選取 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="d825b-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="d825b-111">在 [ **動作** ] 功能表上，指向 [ **新增**]，然後按一下 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="d825b-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="d825b-112">您也可以用滑鼠右鍵按一下 [ **元件** ] 資料夾，指向 [ **新增**]，然後按一下 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="d825b-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="d825b-113">在 [COM + 應用程式安裝精靈] 的 [ **歡迎使用** ] 頁面上，按 [ **下一步**]，然後在 [匯 **入或安裝元件** ] 對話方塊中，按一下 [ **安裝新元件** ]。</span><span class="sxs-lookup"><span data-stu-id="d825b-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="d825b-114">在 [ **安裝新元件** ] 對話方塊中， **按一下 [新增]** 以流覽您要新增的元件。</span><span class="sxs-lookup"><span data-stu-id="d825b-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="d825b-115">在 [ **選取要安裝** 的檔案] 對話方塊中，輸入要安裝的元件檔案名，或從顯示的清單中選取檔案名。</span><span class="sxs-lookup"><span data-stu-id="d825b-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="d825b-116">按一下 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="d825b-116">Click **Open**.</span></span>

    <span data-ttu-id="d825b-117">新增檔案之後，[ **安裝新元件** ] 對話方塊會顯示您已新增的檔案及其相關聯的元件。</span><span class="sxs-lookup"><span data-stu-id="d825b-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="d825b-118">如果您選取 [ **詳細資料** ] 核取方塊，將會看到有關檔案內容和所找到元件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d825b-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="d825b-119">未設定的 COM 元件必須有類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="d825b-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="d825b-120">如果 COM + 找不到元件的類型程式庫，您的元件將不會出現在清單中。</span><span class="sxs-lookup"><span data-stu-id="d825b-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="d825b-121">您也可以選取檔案，然後按一下 [**移除**]，將檔案從 [**要安裝** 的檔案] 清單中移除。</span><span class="sxs-lookup"><span data-stu-id="d825b-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="d825b-122">按 **[下一步**]，然後按一下 **[完成]** 以安裝元件。</span><span class="sxs-lookup"><span data-stu-id="d825b-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d825b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="d825b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d825b-124">複製元件</span><span class="sxs-lookup"><span data-stu-id="d825b-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="d825b-125">建立新的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="d825b-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="d825b-126">刪除 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="d825b-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="d825b-127">匯入元件</span><span class="sxs-lookup"><span data-stu-id="d825b-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="d825b-128">移動元件</span><span class="sxs-lookup"><span data-stu-id="d825b-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="d825b-129">從 COM + 應用程式移除元件</span><span class="sxs-lookup"><span data-stu-id="d825b-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



