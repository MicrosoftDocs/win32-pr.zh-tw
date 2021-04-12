---
description: 在 Windows Installer 中建立對話方塊的程式，類似于使用 Microsoft Windows API 對話方塊範本，以程式設計方式建立對話方塊的流程。
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: 對話方塊總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319511"
---
# <a name="dialog-box-overview"></a><span data-ttu-id="a8f0e-103">對話方塊總覽</span><span class="sxs-lookup"><span data-stu-id="a8f0e-103">Dialog Box Overview</span></span>

<span data-ttu-id="a8f0e-104">在 Windows Installer 中建立對話方塊的程式，類似于使用 Microsoft Windows API 對話方塊範本，以程式設計方式建立對話方塊的流程。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-104">The process of creating a dialog box in Windows Installer is similar to the process of creating a dialog box programmatically using a Microsoft Windows API dialog box template.</span></span> <span data-ttu-id="a8f0e-105">當 Windows 對話方塊範本儲存在以 null 結束的字元字串中時，Windows Installer 會將對話方塊參數儲存在對話方塊資料表中。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-105">While a Windows dialog box template is stored in a null terminated–character string, Windows Installer stores the dialog box parameters in the Dialog table.</span></span> <span data-ttu-id="a8f0e-106">對話方塊資料表所包含的屬性資料行，類似于 Microsoft Windows 使用者介面 API 中的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-106">The Dialog table contains an attributes column that is analogous to Window styles in the Microsoft Windows user interface API.</span></span> <span data-ttu-id="a8f0e-107">不過，Windows Installer 中的對話方塊樣式位數目是縮減且特製化的集合。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-107">However, the number of dialog style bits in Windows Installer is a reduced and specialized set.</span></span>

<span data-ttu-id="a8f0e-108">若要使用 Windows 使用者介面 API 實際建立對話方塊，會呼叫 [**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa) ，並將指標傳遞至範本。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-108">To physically create the dialog box using the Windows user interface API, [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) is called and passes a pointer to the template.</span></span> <span data-ttu-id="a8f0e-109">在 Windows Installer 中，此對話方塊會在執行三個 UI 順序資料表的其中一個時建立。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-109">In Windows Installer, the dialog box is created during execution of one of the three UI sequence tables.</span></span>

<span data-ttu-id="a8f0e-110">Windows Installer 不包含封裝作者可利用其套件的預設 UI。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-110">Windows Installer does not contain a default UI that package authors can utilize for their packages.</span></span> <span data-ttu-id="a8f0e-111">它包含一組有限的預設對話方塊，可顯示錯誤和資訊訊息，但只有在 Windows Installer 查詢對話方塊和 UI 順序資料表，且找不到可用的自訂對話方塊時，才會顯示這些對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-111">It does contain a limited set of default dialog boxes that display error and information messages, but these are displayed only if Windows Installer queries the Dialog and UI Sequence tables and finds there are no custom dialog boxes available.</span></span>

<span data-ttu-id="a8f0e-112">安裝程式 SDK 包含名為 Uisample.msi 的最基本資料庫，其中包含已填入的 UI 和執行順序資料表，以及完整的 UI。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-112">The installer SDK includes a minimal database named Uisample.msi that contains populated UI and execution sequence tables and a complete UI.</span></span> <span data-ttu-id="a8f0e-113">您可以輕鬆地自訂此資料庫，並將其合併至任何套件。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-113">This database is easily customized and merged on to any package.</span></span>

<span data-ttu-id="a8f0e-114">某些標準動作和內部 Windows Installer 錯誤狀況會傳回一組特定的 UI 資料，因此需要有一組特定控制項的對話方塊來容納該資料。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-114">Some standard actions and internal Windows Installer error conditions return a specific set of UI data and therefore require a dialog box with a specific set of controls to accommodate that data.</span></span> <span data-ttu-id="a8f0e-115">Windows Installer 會檢查兩個不同的位置，以取得這些對話方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-115">Windows Installer checks two separate locations for the identifiers for these dialog boxes.</span></span>

-   <span data-ttu-id="a8f0e-116">Windows Installer 包含一組內嵌的對話方塊名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-116">Windows Installer contains a set of embedded dialog box names.</span></span> <span data-ttu-id="a8f0e-117">自訂動作會查詢對話方塊資料表中的這些保留名稱。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-117">The custom action queries the Dialog table for these reserved names.</span></span>
-   <span data-ttu-id="a8f0e-118">在三個 UI 順序資料表中，會顯示序號為-1、-2 或-3 的對話名稱，以回應結束、使用者要求結束，以及來自 Windows Installer 的嚴重錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-118">In each of the three UI sequence tables, dialog names with a sequence number of -1,-2, or -3 are displayed in response to exit, user requested exit, and fatal error messages from Windows Installer.</span></span>

<span data-ttu-id="a8f0e-119">您可以在 [對話方塊](dialog-boxes.md)中找到完整的保留主鍵對話方塊名稱清單。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-119">A complete list of reserved primary key dialog box names is available in [dialog boxes](dialog-boxes.md).</span></span> <span data-ttu-id="a8f0e-120">請注意，主要索引鍵對話方塊名稱只會由安裝程式保留，且 Windows Installer 內不會有對話方塊的特定執行。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-120">Note that the primary key dialog box name is only reserved by the installer and there is no specific implementation of the dialog box within Windows Installer.</span></span> <span data-ttu-id="a8f0e-121">封裝作者仍然必須填入資料庫中的所有欄位，以指定這些保留對話方塊的屬性和控制項。</span><span class="sxs-lookup"><span data-stu-id="a8f0e-121">Package authors must still populate all the fields in the database that specify the attributes and controls of these reserved dialog boxes.</span></span>

 

 
