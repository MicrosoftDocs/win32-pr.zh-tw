---
description: 對話方塊是在對話方塊資料表的對話方塊資料行中指定。 如需在使用者介面中新增對話方塊或佈告欄的詳細資訊，請參閱使用消費者介面。
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: '對話方塊 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193495"
---
# <a name="dialog-boxes-windows-installer"></a><span data-ttu-id="ad0df-104">對話方塊 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="ad0df-104">Dialog Boxes (Windows Installer)</span></span>

<span data-ttu-id="ad0df-105">對話方塊是在 [對話方塊資料表](dialog-table.md)的對話方塊資料行中指定。</span><span class="sxs-lookup"><span data-stu-id="ad0df-105">Dialog boxes are specified in the Dialog column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="ad0df-106">如需在使用者介面中新增對話方塊或佈告欄的詳細資訊，請參閱 [使用消費者介面](using-the-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="ad0df-106">For more information on adding a dialog box or billboard to a user interface, see [Using the User Interface](using-the-user-interface.md).</span></span>

## <a name="reserved-dialog-box-names"></a><span data-ttu-id="ad0df-107">保留的對話方塊名稱</span><span class="sxs-lookup"><span data-stu-id="ad0df-107">Reserved Dialog Box Names</span></span>

<span data-ttu-id="ad0df-108">下列對話方塊名稱是由 Windows Installer 保留，不能用於任何使用者撰寫的自訂對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ad0df-108">The following dialog box names are reserved by Windows Installer and should not be used for any user-authored custom dialog boxes.</span></span> <span data-ttu-id="ad0df-109">安裝程式會要求在 [對話方塊資料表](dialog-table.md) 中，使用下列保留名稱來列出這些對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ad0df-109">The installer requires that these dialog boxes be listed in the [Dialog table](dialog-table.md) using the following reserved names.</span></span> <span data-ttu-id="ad0df-110">每個對話方塊和名稱只能列出一次。</span><span class="sxs-lookup"><span data-stu-id="ad0df-110">Each dialog box and name can only be listed once.</span></span> <span data-ttu-id="ad0df-111">開發人員必須在使用者介面中撰寫這些對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ad0df-111">Developers must author these dialog boxes into the user interface.</span></span> <span data-ttu-id="ad0df-112">如需如何預覽對話方塊的詳細資訊，請參閱匯 [入消費者介面](importing-the-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="ad0df-112">For information about how to preview dialog boxes, see [Importing the User Interface](importing-the-user-interface.md).</span></span>



| <span data-ttu-id="ad0df-113">對話方塊名稱</span><span class="sxs-lookup"><span data-stu-id="ad0df-113">Dialog box name</span></span>                                      | <span data-ttu-id="ad0df-114">對話方塊的簡短描述</span><span class="sxs-lookup"><span data-stu-id="ad0df-114">Brief description of dialog box</span></span>                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad0df-115">FilesInUse 對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-115">FilesInUse Dialog</span></span>](filesinuse-dialog.md)           | <span data-ttu-id="ad0df-116">警示使用者進程覆寫或刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="ad0df-116">Alerts user to processes overwriting or deleting files.</span></span>                                                                                                                 |
| [<span data-ttu-id="ad0df-117">Firstrun.cmd 對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-117">FirstRun Dialog</span></span>](firstrun-dialog.md)               | <span data-ttu-id="ad0df-118">收集使用者名稱、公司名稱和產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad0df-118">Collects user name, company name, and product ID.</span></span>                                                                                                                       |
| [<span data-ttu-id="ad0df-119">MsiRMFilesInUse 對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-119">MsiRMFilesInUse Dialog</span></span>](msirmfilesinuse-dialog.md) | <span data-ttu-id="ad0df-120">警示使用者處理覆寫或刪除檔案，並讓使用者可以選擇使用 [重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal) 來關閉和重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="ad0df-120">Alerts the user to processes overwriting or deleting files and gives the user the option to use the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to close and restart applications.</span></span> |



 

## <a name="required-dialog-boxes"></a><span data-ttu-id="ad0df-121">必要對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-121">Required Dialog Boxes</span></span>

<span data-ttu-id="ad0df-122">在安裝期間，某些事件會導致 Windows Installer 檢查封裝中的 [使用者介面順序資料表](using-a-sequence-table.md) ，並顯示指定的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ad0df-122">During the installation, certain events cause Windows Installer to check the [user interface sequence tables](using-a-sequence-table.md) in the package and display the specified dialog box.</span></span> <span data-ttu-id="ad0df-123">例如，在發生嚴重錯誤的情況下，Windows Installer 會顯示在使用者介面順序資料表中，以-3 序號列出的對話方塊，不論對話方塊 [資料表](dialog-table.md)中該對話方塊的名稱為何。</span><span class="sxs-lookup"><span data-stu-id="ad0df-123">For example, in the case of a fatal error, Windows Installer displays the dialog box that is listed with a sequence number of -3 in the user interface sequence table regardless of what that dialog box is named in the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="ad0df-124">下表列出特定事件，以及其在使用者介面順序資料表中的對應序號：</span><span class="sxs-lookup"><span data-stu-id="ad0df-124">The following table lists the specific events and their corresponding sequence number in the user interface sequence table:</span></span>



| <span data-ttu-id="ad0df-125">事件種類</span><span class="sxs-lookup"><span data-stu-id="ad0df-125">Type of Event</span></span>                        | <span data-ttu-id="ad0df-126">使用者介面順序資料表序號</span><span class="sxs-lookup"><span data-stu-id="ad0df-126">User interface sequence table sequence number</span></span> | <span data-ttu-id="ad0df-127">對話方塊的描述</span><span class="sxs-lookup"><span data-stu-id="ad0df-127">Description of dialog box</span></span>                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ad0df-128">嚴重錯誤</span><span class="sxs-lookup"><span data-stu-id="ad0df-128">Fatal error</span></span>](fatalerror-dialog.md) | <span data-ttu-id="ad0df-129">-3</span><span class="sxs-lookup"><span data-stu-id="ad0df-129">-3</span></span>                                            | <span data-ttu-id="ad0df-130">安裝因嚴重錯誤而終止。</span><span class="sxs-lookup"><span data-stu-id="ad0df-130">The installation was terminated by a fatal error.</span></span>      |
| [<span data-ttu-id="ad0df-131">使用者離開</span><span class="sxs-lookup"><span data-stu-id="ad0df-131">User exit</span></span>](userexit-dialog.md)     | <span data-ttu-id="ad0df-132">-2</span><span class="sxs-lookup"><span data-stu-id="ad0df-132">-2</span></span>                                            | <span data-ttu-id="ad0df-133">已在使用者的要求結束安裝。</span><span class="sxs-lookup"><span data-stu-id="ad0df-133">The installation was terminated at the user's request.</span></span> |
| [<span data-ttu-id="ad0df-134">結束</span><span class="sxs-lookup"><span data-stu-id="ad0df-134">Exit</span></span>](exit-dialog.md)              | <span data-ttu-id="ad0df-135">-1</span><span class="sxs-lookup"><span data-stu-id="ad0df-135">-1</span></span>                                            | <span data-ttu-id="ad0df-136">安裝已順利完成。</span><span class="sxs-lookup"><span data-stu-id="ad0df-136">The installation completed successfully.</span></span>               |



 

<span data-ttu-id="ad0df-137">此外，封裝作者必須建立一般對話方塊來顯示 Windows Installer [錯誤](error-dialog.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="ad0df-137">In addition, the package author must create a generic dialog box to display Windows Installer [error](error-dialog.md) messages.</span></span> <span data-ttu-id="ad0df-138">此對話方塊可以命名為任何名稱，但必須在 **ErrorDialog** 屬性中指定這個名稱。</span><span class="sxs-lookup"><span data-stu-id="ad0df-138">This dialog box can be named anything, but this name must be specified in the **ErrorDialog** property.</span></span>

## <a name="typical-dialog-boxes"></a><span data-ttu-id="ad0df-139">一般對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-139">Typical Dialog Boxes</span></span>

<span data-ttu-id="ad0df-140">下列對話方塊是選擇性的，通常包含在安裝套件的撰寫使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="ad0df-140">The following dialog boxes are optional and are commonly included in the authored user interface of an installation package.</span></span> <span data-ttu-id="ad0df-141">這些對話方塊通常是安裝檔案的大部分 [使用者介面嚮導](user-interface-wizard-behavior.md) 。</span><span class="sxs-lookup"><span data-stu-id="ad0df-141">These dialogs are typical of most [user interface wizards](user-interface-wizard-behavior.md) for installing files.</span></span> <span data-ttu-id="ad0df-142">這些對話方塊在對話方塊資料表中可以有任何名稱。</span><span class="sxs-lookup"><span data-stu-id="ad0df-142">These dialog boxes can have any name in the Dialog table.</span></span> <span data-ttu-id="ad0df-143">所顯示的名稱只建議用來清楚起見，而且可以視需要進行修改。</span><span class="sxs-lookup"><span data-stu-id="ad0df-143">The names shown are only recommended for clarity and can be modified as necessary.</span></span> <span data-ttu-id="ad0df-144">例如，您可以在封裝中使用兩個不同的自訂 **LicenseAgreement** 對話方塊，並依名稱 ProfessionalLicenseAgreement 和 LimitedLicenseAgreement 來辨別對話方塊資料表。</span><span class="sxs-lookup"><span data-stu-id="ad0df-144">For example, two different custom **LicenseAgreement** dialog boxes can be used in the package and distinguished in the Dialog table by the names ProfessionalLicenseAgreement and LimitedLicenseAgreement.</span></span>



| <span data-ttu-id="ad0df-145">對話方塊類型</span><span class="sxs-lookup"><span data-stu-id="ad0df-145">Dialog box type</span></span>                                             | <span data-ttu-id="ad0df-146">對話方塊的簡短描述</span><span class="sxs-lookup"><span data-stu-id="ad0df-146">Brief description of dialog box</span></span>                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="ad0df-147">DiskCost 對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-147">DiskCost dialog box</span></span>](diskcost-dialog.md)                  | <span data-ttu-id="ad0df-148">指出沒有足夠的磁碟空間可供安裝。</span><span class="sxs-lookup"><span data-stu-id="ad0df-148">Indicates insufficient disk space for the installation.</span></span> |
| [<span data-ttu-id="ad0df-149">瀏覽對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-149">Browse dialog box</span></span>](browse-dialog.md)                      | <span data-ttu-id="ad0df-150">可讓使用者選取目錄。</span><span class="sxs-lookup"><span data-stu-id="ad0df-150">Enables user to select a directory.</span></span>                     |
| [<span data-ttu-id="ad0df-151">取消對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-151">Cancel dialog box</span></span>](cancel-dialog.md)                      | <span data-ttu-id="ad0df-152">確認終止安裝的要求。</span><span class="sxs-lookup"><span data-stu-id="ad0df-152">Confirms a request to terminate the installation.</span></span>       |
| [<span data-ttu-id="ad0df-153">授權合約對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-153">License agreement dialog box</span></span>](licenseagreement-dialog.md) | <span data-ttu-id="ad0df-154">顯示授權合約的模式方塊。</span><span class="sxs-lookup"><span data-stu-id="ad0df-154">Modal box displaying the license agreement.</span></span>             |
| [<span data-ttu-id="ad0df-155">選取對話方塊</span><span class="sxs-lookup"><span data-stu-id="ad0df-155">Selection dialog box</span></span>](selection-dialog.md)                | <span data-ttu-id="ad0df-156">讓使用者選取專案的模式方塊。</span><span class="sxs-lookup"><span data-stu-id="ad0df-156">Modal box enabling the user to select items.</span></span>            |



 

 

 
