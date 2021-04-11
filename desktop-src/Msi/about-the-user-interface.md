---
description: Windows Installer 包含的功能，可讓安裝套件開發人員撰寫圖形化使用者介面 (GUI) ，在安裝期間對使用者顯示。
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: 關於消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848997"
---
# <a name="about-the-user-interface"></a><span data-ttu-id="ebea1-103">關於消費者介面</span><span class="sxs-lookup"><span data-stu-id="ebea1-103">About the User Interface</span></span>

<span data-ttu-id="ebea1-104">Windows Installer 包含的功能，可讓安裝套件開發人員撰寫圖形化使用者介面 (GUI) ，在安裝期間對使用者顯示。</span><span class="sxs-lookup"><span data-stu-id="ebea1-104">Windows Installer contains functionality that enables installation package developers to author a graphical user interface (GUI) that is displayed to the end-user during installation.</span></span> <span data-ttu-id="ebea1-105">此使用者介面可以展示 [使用者介面 wizard 的行為](user-interface-wizard-behavior.md)、顯示對話方塊和公告欄，以及在安裝期間對使用者呈現互動式控制項。</span><span class="sxs-lookup"><span data-stu-id="ebea1-105">This user interface can exhibit [user interface wizard behavior](user-interface-wizard-behavior.md), display dialog boxes and billboards, and present interactive controls to users during the installation.</span></span>

<span data-ttu-id="ebea1-106">安裝程式內部 UI 是透過 Windows Installer 本身內的一組資料庫資料表來管理和控制。</span><span class="sxs-lookup"><span data-stu-id="ebea1-106">The installer internal UI is managed and controlled through a set of database tables within Windows Installer itself.</span></span> <span data-ttu-id="ebea1-107">安裝程式只會提供一組用於處理錯誤和資訊訊息的預設對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ebea1-107">The installer provides only a small set of default dialog boxes that are intended to handle error and information messages.</span></span> <span data-ttu-id="ebea1-108">所有自訂對話方塊都必須由封裝作者建立。</span><span class="sxs-lookup"><span data-stu-id="ebea1-108">All custom dialog boxes must be created by the package author.</span></span>

<span data-ttu-id="ebea1-109">沒有特定的 Windows Installer API 可讓套件作者以程式設計方式建立 UI。</span><span class="sxs-lookup"><span data-stu-id="ebea1-109">There is no specific Windows Installer API to allow a package author to create a UI programmatically.</span></span> <span data-ttu-id="ebea1-110">您可以使用 Microsoft Windows API 以程式設計方式建立 UI;不過，建議套件作者使用提供的內部 UI。</span><span class="sxs-lookup"><span data-stu-id="ebea1-110">It is possible to use the Microsoft Windows API to create a UI programmatically; however, it is recommended that package authors use the internal UI provided.</span></span>

<span data-ttu-id="ebea1-111">安裝程式套件作者建立自訂對話方塊的方式，是將其自訂對話方塊的名稱輸入 \_ 對話方塊資料表的 "dialog" 資料行，並使用其餘的資料行來指定大小、位置和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="ebea1-111">Installer package authors create custom dialog boxes by entering the name of their custom dialog into the "\_Dialog" column of the dialog table and specifying the size, position, and other attributes using the remaining columns.</span></span>

<span data-ttu-id="ebea1-112">Windows Installer 也會執行封裝作者可放置在對話方塊上的一些標準控制項。</span><span class="sxs-lookup"><span data-stu-id="ebea1-112">Windows Installer also implements a number of standard controls that a package author can place onto dialog boxes.</span></span> <span data-ttu-id="ebea1-113">並非所有標準的 Microsoft Windows 控制項都可使用，而且無法建立自訂控制項以搭配安裝程式 UI 使用。</span><span class="sxs-lookup"><span data-stu-id="ebea1-113">Not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="ebea1-114">您可以在特定的對話方塊上建立控制項，方法是輸入對話方塊名稱、對話方塊資料表中對話方塊專案的主鍵、控制項資料表的第二個欄位，以及使用其餘的資料行來指定控制項的大小、位置和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="ebea1-114">Controls are created on a specific dialog box by entering the name of the dialog box, the primary key to the dialog box's entry in the dialog table, into the second field of the control table and specifying the control's size, position, and other attributes using the remaining columns.</span></span>

<span data-ttu-id="ebea1-115">現用控制項必須連結至 [ControlEvent 資料表](controlevent-table.md) 中的 ControlEvent，以允許使用者與安裝互動。</span><span class="sxs-lookup"><span data-stu-id="ebea1-115">Active controls must be linked to a ControlEvent in the [ControlEvent table](controlevent-table.md) to allow user interaction with the installation.</span></span> <span data-ttu-id="ebea1-116">接收和顯示資訊的被動控制項必須訂閱 [EventMapping 資料表](eventmapping-table.md)中適當的 ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="ebea1-116">Passive controls that receive and display information must be subscribed to an appropriate ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ebea1-117">如需有關事件的詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ebea1-117">For more information about ControlEvents, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="ebea1-118">請注意，如果在 ControlEvent 資料表中列出某個控制項，並且訂閱了 EventMapping 資料表中所列的事件，控制項就會發行 ControlEvent。</span><span class="sxs-lookup"><span data-stu-id="ebea1-118">Note that a control publishes a ControlEvent if listed in the ControlEvent table and subscribes to an event if listed in the EventMapping table.</span></span>

<span data-ttu-id="ebea1-119">安裝期間的安裝程式 UI 會透過 UI 順序資料表來管理： [InstallUISequence 資料表](installuisequence-table.md)和 [AdminUISequence 資料表](adminuisequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="ebea1-119">The installer UI display during installation is managed through the UI sequence tables: [InstallUISequence Table](installuisequence-table.md), and [AdminUISequence Table](adminuisequence-table.md).</span></span> <span data-ttu-id="ebea1-120">系統會根據起始安裝的最上層動作，執行下列其中一個順序資料表： [安裝](install-action.md)、系統 [管理員](admin-action.md)或 [公告](advertise-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ebea1-120">One of these sequence tables is executed depending on the top-level action that initiated the installation: [INSTALL](install-action.md), [ADMIN](admin-action.md), or [ADVERTISE](advertise-action.md).</span></span>

<span data-ttu-id="ebea1-121">如需在 Windows Installer 中執行 UI 的詳細資訊，請參閱 [使用消費者介面](using-the-user-interface.md)、 [消費者介面架構](user-interface-schema.md)，以及對話方塊和控制項的個別主題。</span><span class="sxs-lookup"><span data-stu-id="ebea1-121">For more information about implementing a UI in Windows Installer, please see [Using the User Interface](using-the-user-interface.md), [User Interface Schema](user-interface-schema.md), as well as the individual topics for dialog boxes and controls.</span></span>

 

 



