---
description: 當安裝 Windows Installer 套件時不需要提高許可權時，套件的作者可以隱藏 [使用者帳戶控制] (UAC) 顯示的對話方塊，以提示使用者提供系統管理員授權。
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: 在不含 UAC 對話方塊的情況下撰寫套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692795"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="fc57d-103">在不含 UAC 對話方塊的情況下撰寫套件</span><span class="sxs-lookup"><span data-stu-id="fc57d-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="fc57d-104">當安裝 Windows Installer 套件時不需要提高許可權時，套件的作者可以隱藏 [ [*使用者帳戶控制*](u-gly.md) ] (UAC) 顯示的對話方塊，以提示使用者提供系統管理員授權。</span><span class="sxs-lookup"><span data-stu-id="fc57d-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="fc57d-105">若要在安裝應用程式時抑制 UAC 對話方塊的顯示，封裝的作者應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="fc57d-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="fc57d-106">在 Windows Vista 上使用 Window Installer 4.0 或更新版本安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="fc57d-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="fc57d-107">請勿依賴使用提升的系統許可權在電腦上安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="fc57d-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="fc57d-108">在每個使用者的內容中安裝應用程式，並使其成為封裝的預設安裝內容。</span><span class="sxs-lookup"><span data-stu-id="fc57d-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="fc57d-109">如果未設定 [**ALLUSERS**](allusers.md) 屬性，安裝程式就會在每個使用者的內容中安裝套件。</span><span class="sxs-lookup"><span data-stu-id="fc57d-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="fc57d-110">如果您未在 [屬性工作表](property-table.md)中包含 **ALLUSERS** 屬性，安裝程式就不會設定這個屬性，因此每個使用者安裝都會變成預設的安裝內容。</span><span class="sxs-lookup"><span data-stu-id="fc57d-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="fc57d-111">您可以藉由在命令列上設定 **ALLUSERS** 屬性來覆寫這個預設值。</span><span class="sxs-lookup"><span data-stu-id="fc57d-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="fc57d-112">在 [ [**字數統計摘要**](word-count-summary.md) ] 屬性中設定位3，表示安裝應用程式時不需要提高的許可權。</span><span class="sxs-lookup"><span data-stu-id="fc57d-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



