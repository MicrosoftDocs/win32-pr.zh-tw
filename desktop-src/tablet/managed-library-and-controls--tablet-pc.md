---
description: 若要在 C 和 Visual Basic .NET 中建立 Tablet PC 應用程式 \# ，Microsoft Visual Studio .net 中的專案必須包含 TABLET pc 受管理程式庫元件的參考。 這可讓您存取 managed 物件模型和控制項。
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: '受管理的程式庫和控制項 (Tablet PC) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997187"
---
# <a name="managed-library-and-controls-tablet-pc"></a><span data-ttu-id="e0fad-104">受管理的程式庫和控制項 (Tablet PC) </span><span class="sxs-lookup"><span data-stu-id="e0fad-104">Managed Library and Controls (Tablet PC)</span></span>

<span data-ttu-id="e0fad-105">若要在 C 和 Visual Basic .NET 中建立 Tablet PC 應用程式 \# ，Microsoft Visual Studio .net 中的專案必須包含 TABLET pc 受管理程式庫元件的參考。</span><span class="sxs-lookup"><span data-stu-id="e0fad-105">To build Tablet PC applications in C\# and Visual Basic .NET, your project in Microsoft Visual Studio .NET must include a reference to the Tablet PC managed library assemblies.</span></span> <span data-ttu-id="e0fad-106">這可讓您存取 managed 物件模型和控制項。</span><span class="sxs-lookup"><span data-stu-id="e0fad-106">This provides access to the managed object model and controls.</span></span>

## <a name="microsoft-visual-c-and-visual-basicnet"></a><span data-ttu-id="e0fad-107">Microsoft Visual C \# 和 visual Basic.NET</span><span class="sxs-lookup"><span data-stu-id="e0fad-107">Microsoft Visual C\# and Visual Basic.NET</span></span>

<span data-ttu-id="e0fad-108">在 Windows Vista 中，Tablet PC managed 程式庫元件預設會安裝在兩個目錄中：</span><span class="sxs-lookup"><span data-stu-id="e0fad-108">In Windows Vista, the Tablet PC managed library assemblies are installed by default in two directories:</span></span>

-   <span data-ttu-id="e0fad-109"><systemdrive>： \\ Program files \\ 一般檔案 \\ Microsoft 共用 \\ 筆墨目錄</span><span class="sxs-lookup"><span data-stu-id="e0fad-109"><systemdrive>:\\Program Files\\Common Files\\Microsoft Shared\\Ink directory</span></span>
-   <span data-ttu-id="e0fad-110"><systemdrive>： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ Bin</span><span class="sxs-lookup"><span data-stu-id="e0fad-110"><systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Bin</span></span>

<span data-ttu-id="e0fad-111">若要在 Microsoft Visual Studio .NET 中新增 Tablet PC 平臺受控程式庫的參考：</span><span class="sxs-lookup"><span data-stu-id="e0fad-111">To add a reference to the Tablet PC platform managed libraries in Microsoft Visual Studio .NET:</span></span>

1.  <span data-ttu-id="e0fad-112">開啟您的 Visual Studio .NET 專案。</span><span class="sxs-lookup"><span data-stu-id="e0fad-112">Open your Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="e0fad-113">在 [專案] 功能表上，按一下 [加入參考]。</span><span class="sxs-lookup"><span data-stu-id="e0fad-113">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="e0fad-114">在 [**加入參考**] 對話方塊的 [ **.net** ] 索引標籤上，選取 [元件] 清單中的 [ **Microsoft Tablet PC API**]。</span><span class="sxs-lookup"><span data-stu-id="e0fad-114">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC API**.</span></span>
4.  <span data-ttu-id="e0fad-115">按一下 [ **選取**]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="e0fad-115">Click **Select**, and then click **OK**.</span></span>

<span data-ttu-id="e0fad-116">若要在 Visual Studio .NET 中加入筆墨分析 Api 的參考：</span><span class="sxs-lookup"><span data-stu-id="e0fad-116">To add a reference to the ink analysis APIs in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="e0fad-117">開啟您的 Microsoft Visual Studio .NET 專案。</span><span class="sxs-lookup"><span data-stu-id="e0fad-117">Open your Microsoft Visual Studio .NET project.</span></span>
2.  <span data-ttu-id="e0fad-118">在 [專案] 功能表上，按一下 [加入參考]。</span><span class="sxs-lookup"><span data-stu-id="e0fad-118">On the **Project** menu, click **Add Reference**.</span></span>
3.  <span data-ttu-id="e0fad-119">在 [**加入參考**] 對話方塊的 [ **.net** ] 索引標籤上，選取 [元件] 清單中的 [ **Microsoft Tablet PC 筆墨分析 Managed 程式庫**]。</span><span class="sxs-lookup"><span data-stu-id="e0fad-119">On the **.NET** tab in the **Add Reference** dialog box, on the components list, select **Microsoft Tablet PC Ink Analysis Managed Library**.</span></span>
4.  <span data-ttu-id="e0fad-120">按一下 [ **選取**]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="e0fad-120">Click **Select**, and then click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="e0fad-121">在 Visual Studio 2005 編譯使用 Microsoft 的應用程式時，您必須選取 [ **專案**]，選取 [ **屬性**]，選取 [ **組建** ] 和 [設定平臺目標 = x86]。</span><span class="sxs-lookup"><span data-stu-id="e0fad-121">When compiling applications that use Microsoft.Ink on Visual Studio 2005, you must select **Project**, select **Properties**, select **Build** and set Platform target=x86.</span></span> <span data-ttu-id="e0fad-122">此選項不適用於 Microsoft Visual Studio Express 產品。</span><span class="sxs-lookup"><span data-stu-id="e0fad-122">This option is not available in Microsoft Visual Studio Express products.</span></span>

 

 

 



