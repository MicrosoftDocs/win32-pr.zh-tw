---
description: 您可以使用 [元件服務] 系統管理工具，將已在電腦上註冊的應用程式特定元件匯入至 Windows 登錄中的 COM 元件。
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: 匯入元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468104"
---
# <a name="importing-components"></a><span data-ttu-id="2aa91-103">匯入元件</span><span class="sxs-lookup"><span data-stu-id="2aa91-103">Importing Components</span></span>

<span data-ttu-id="2aa91-104">您可以使用 [元件服務] 系統管理工具，將已在電腦上註冊的應用程式特定元件匯入至 Windows 登錄中的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="2aa91-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="2aa91-105">匯入元件並不會安裝設定介面屬性所需的介面或方法資訊，或是設定遠端用戶端對元件的存取。</span><span class="sxs-lookup"><span data-stu-id="2aa91-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="2aa91-106">因此，可能的話，您應該安裝而非匯入未設定的元件。</span><span class="sxs-lookup"><span data-stu-id="2aa91-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="2aa91-107">當匯入元件至 COM + 應用程式時，COM + 不會填入元件的介面和方法資訊。</span><span class="sxs-lookup"><span data-stu-id="2aa91-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="2aa91-108">在匯出應用程式 proxy 期間，COM + 將不會提供封送處理資訊 (類型程式庫或 proxy/存根) 適用于部分或所有介面。</span><span class="sxs-lookup"><span data-stu-id="2aa91-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="2aa91-109">匯出包含已匯入元件的應用程式 proxy 將會失敗，或導致發出警告。</span><span class="sxs-lookup"><span data-stu-id="2aa91-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="2aa91-110">**將元件匯入至 COM + 應用程式**</span><span class="sxs-lookup"><span data-stu-id="2aa91-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="2aa91-111">在 [元件服務] 系統管理工具的主控台樹中，選取裝載 COM + 應用程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="2aa91-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="2aa91-112">開啟該電腦的 [ **Com + 應用程式** ] 資料夾，然後選取您要在其中安裝元件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2aa91-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="2aa91-113">開啟應用程式資料夾，然後選取 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="2aa91-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="2aa91-114">在 [ **動作** ] 功能表上，指向 [ **新增**]，然後按一下 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="2aa91-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="2aa91-115">您也可以用滑鼠右鍵按一下 [ **元件** ] 資料夾，指向 [ **新增**]，然後按一下 [ **元件**]。</span><span class="sxs-lookup"><span data-stu-id="2aa91-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="2aa91-116">在 [COM + 應用程式安裝精靈] 的 [ **歡迎使用** ] 頁面上，按 [ **下一步**]，然後在 [匯 **入或安裝元件** ] 對話方塊中，按一下 **已註冊的 [匯入元件 (s])**。</span><span class="sxs-lookup"><span data-stu-id="2aa91-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="2aa91-117">在 [ **選擇要匯入的元件** ] 對話方塊中，選取 [ **詳細資料** ] 核取方塊以查看已註冊之元件的完整資訊。</span><span class="sxs-lookup"><span data-stu-id="2aa91-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="2aa91-118">從顯示的清單中選取您要匯入的元件 () ，然後按 [ **下一步]**。</span><span class="sxs-lookup"><span data-stu-id="2aa91-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="2aa91-119">按一下 [完成] 。</span><span class="sxs-lookup"><span data-stu-id="2aa91-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aa91-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="2aa91-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aa91-121">複製元件</span><span class="sxs-lookup"><span data-stu-id="2aa91-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="2aa91-122">建立新的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="2aa91-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="2aa91-123">刪除 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="2aa91-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="2aa91-124">安裝新元件</span><span class="sxs-lookup"><span data-stu-id="2aa91-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="2aa91-125">移動元件</span><span class="sxs-lookup"><span data-stu-id="2aa91-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="2aa91-126">從 COM + 應用程式移除元件</span><span class="sxs-lookup"><span data-stu-id="2aa91-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



