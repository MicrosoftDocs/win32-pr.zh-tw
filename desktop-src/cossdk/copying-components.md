---
description: 您可以將元件從一個 COM + 應用程式複製到另一個 COM + 應用程式。 將元件複製到另一個 COM + 應用程式之後，您可以設定此元件的方式與原始元件不同。
ms.assetid: 49dfd449-05eb-4442-989f-15bc1586d8c5
title: 複製元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2224c42e9891c67999934062a50cd2215da2adc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510550"
---
# <a name="copying-components"></a><span data-ttu-id="3a0f4-104">複製元件</span><span class="sxs-lookup"><span data-stu-id="3a0f4-104">Copying Components</span></span>

<span data-ttu-id="3a0f4-105">您可以將元件從一個 COM + 應用程式複製到另一個 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-105">You can copy a component from one COM+ application to another.</span></span> <span data-ttu-id="3a0f4-106">將元件複製到另一個 COM + 應用程式之後，您可以設定此元件的方式與原始元件不同。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-106">After you copy a component to another COM+ application, you can configure this component differently than the original component.</span></span>

<span data-ttu-id="3a0f4-107">**將元件從一個 COM + 應用程式複製到另一個 COM + 應用程式**</span><span class="sxs-lookup"><span data-stu-id="3a0f4-107">**To copy a component from one COM+ application to another**</span></span>

1.  <span data-ttu-id="3a0f4-108">在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠右鍵按一下您要複製的元件，然後按一下 [ **複製**]。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-108">In the details pane of the Component Services administrative tool, right-click the component that you want to copy and then click **Copy**.</span></span>

2.  <span data-ttu-id="3a0f4-109">在 [ **複製元件** ] 對話方塊的 [ **請選取目的地** ] 窗格中，選取要將元件複製到其中的 com + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-109">In the **Copy Component** dialog box, in the **Please select a Destination** pane, select the COM+ application to which the component will be copied.</span></span>

3.  <span data-ttu-id="3a0f4-110">輸入所複製元件的新 ProgID。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-110">Enter the new ProgID for the copied component.</span></span>

    > [!Note]  
    > <span data-ttu-id="3a0f4-111">原始元件的 ProgID 會顯示為參考，而且無法變更。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-111">The ProgID for the original component is displayed for reference and cannot be changed.</span></span>

     

4.  <span data-ttu-id="3a0f4-112">輸入所複製元件的新 CLSID。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-112">Enter the new CLSID for the copied component.</span></span> <span data-ttu-id="3a0f4-113">COM + 會顯示自動產生的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-113">COM+ displays an automatically generated CLSID.</span></span> <span data-ttu-id="3a0f4-114">在大部分的情況下，這就足以唯一識別複製的元件。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-114">In most cases, this will be sufficient to uniquely identify the copied component.</span></span> <span data-ttu-id="3a0f4-115">只有在您想要變更 COM + 所提供的 CLSID 時，才輸入新的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-115">Enter a new CLSID only if you want to change the one provided by COM+.</span></span>

5.  <span data-ttu-id="3a0f4-116">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="3a0f4-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a0f4-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a0f4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a0f4-118">建立新的 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="3a0f4-118">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="3a0f4-119">刪除 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="3a0f4-119">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="3a0f4-120">匯入元件</span><span class="sxs-lookup"><span data-stu-id="3a0f4-120">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="3a0f4-121">安裝新元件</span><span class="sxs-lookup"><span data-stu-id="3a0f4-121">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="3a0f4-122">移動元件</span><span class="sxs-lookup"><span data-stu-id="3a0f4-122">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="3a0f4-123">從 COM + 應用程式移除元件</span><span class="sxs-lookup"><span data-stu-id="3a0f4-123">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



