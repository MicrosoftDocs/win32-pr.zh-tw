---
description: 如果必須註冊應用程式，請依照在安裝或移除元件時新增和移除登錄機碼一節中所述的方式來撰寫安裝套件。
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: 新增和移除應用程式，而不在登錄中保留任何追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36804633a51e0e2f4beafc37e9f830e1743a5ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944043"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a><span data-ttu-id="2e89b-103">新增和移除應用程式，而不在登錄中保留任何追蹤</span><span class="sxs-lookup"><span data-stu-id="2e89b-103">Adding and Removing an Application and Leaving No Trace in the Registry</span></span>

<span data-ttu-id="2e89b-104">如果必須註冊應用程式，請依照在 [安裝或移除元件時新增和移除登錄機碼](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)一節中所述的方式來撰寫安裝套件。</span><span class="sxs-lookup"><span data-stu-id="2e89b-104">If an application must be registered, author the installation package as described in the section [Adding and Removing Registry Keys on the Installation or Removal of Components](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md).</span></span> <span data-ttu-id="2e89b-105">註冊是由安裝程式用於公告，以及由主控台中的 [新增或移除程式] 功能使用。</span><span class="sxs-lookup"><span data-stu-id="2e89b-105">Registration is used by the installer for advertisement and by the Add or Remove Programs feature in Control Panel.</span></span> <span data-ttu-id="2e89b-106">如果未註冊應用程式，則無法通告，也不會列在主控台的 [新增或移除程式] 功能中。</span><span class="sxs-lookup"><span data-stu-id="2e89b-106">If an application is not registered, it cannot be advertised, and is not listed in the Add or Remove Programs feature in Control Panel.</span></span>

<span data-ttu-id="2e89b-107">您可以從[InstallExecuteSequence 資料表](installexecutesequence-table.md)和[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中移除[RegisterProduct 動作](registerproduct-action.md)、 [RegisterUser 動作](registeruser-action.md)、 [PublishProduct 動作](publishproduct-action.md)和[PublishFeatures 動作](publishfeatures-action.md)，以省略註冊應用程式。</span><span class="sxs-lookup"><span data-stu-id="2e89b-107">You can omit registering an application by removing the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) from the [InstallExecuteSequence Table](installexecutesequence-table.md) and [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="2e89b-108">所有這些動作都必須移除，否則應用程式的某些追蹤可能會保留在登錄中。</span><span class="sxs-lookup"><span data-stu-id="2e89b-108">All of these actions must be removed, or some trace of the application may remain in the registry.</span></span> <span data-ttu-id="2e89b-109">移除所有這些動作可防止應用程式列在主控台的 [新增或移除程式] 功能中，並防止應用程式的公告。</span><span class="sxs-lookup"><span data-stu-id="2e89b-109">Removing all of these actions prevents the application from being listed in the Add or Remove Programs feature in Control Panel, and prevents the advertisement of the application.</span></span> <span data-ttu-id="2e89b-110">移除所有這些動作也會導致應用程式無法向 Windows Installer 設定資料進行註冊。</span><span class="sxs-lookup"><span data-stu-id="2e89b-110">Removing all of these actions also prevents the application from being registered with the Windows Installer configuration data.</span></span> <span data-ttu-id="2e89b-111">這表示您無法使用 Windows Installer [命令列選項](command-line-options.md)或 Windows Installer 應用程式開發介面 (API) ，來移除、修復或重新安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="2e89b-111">This means that you cannot remove, repair, or reinstall the application by using the Windows Installer [Command-Line Options](command-line-options.md), or the Windows Installer application programming interface (API).</span></span>

<span data-ttu-id="2e89b-112">若要從主控台中的 [新增或移除程式] 功能隱藏應用程式，且仍然能夠使用 Windows Installer 來管理應用程式，請將註冊動作保留在順序資料表中，並將 [屬性工作表](property-table.md)中的 [**ARPSYSTEMCOMPONENT 屬性**](arpsystemcomponent.md)設定為 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="2e89b-112">To hide an application from the Add or Remove Programs feature in Control Panel and still be able to use the Windows Installer to manage an application, leave the registration actions in the sequence tables, and set the [**ARPSYSTEMCOMPONENT Property**](arpsystemcomponent.md) in the [Property Table](property-table.md) to 1 (one).</span></span> <span data-ttu-id="2e89b-113">應用程式不會出現在 [新增或移除程式] 功能中，但您可以使用 Windows Installer 安裝隨選安裝、卸載、修復和重新安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="2e89b-113">The application does not appear in the Add or Remove Programs feature, but you can use the Windows Installer to install-on-demand, uninstall, repair, and reinstall the application.</span></span>

 

 



