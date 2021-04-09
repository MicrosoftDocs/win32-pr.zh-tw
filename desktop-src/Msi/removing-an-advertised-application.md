---
description: 若要移除已在公告狀態下安裝的應用程式，只要使用 MsiInstallProduct 或 MsiConfigureProduct 將它卸載即可。 您也可以從命令列移除已公告的應用程式。 請參閱命令列選項。
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: 移除已公告的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849960"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="1b4de-105">移除已公告的應用程式</span><span class="sxs-lookup"><span data-stu-id="1b4de-105">Removing an Advertised Application</span></span>

<span data-ttu-id="1b4de-106">若要移除已在公告狀態下安裝的應用程式，只要使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 或 [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)將它卸載即可。</span><span class="sxs-lookup"><span data-stu-id="1b4de-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="1b4de-107">您也可以從命令列移除已公告的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b4de-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="1b4de-108">請參閱 [命令列選項](command-line-options.md)。</span><span class="sxs-lookup"><span data-stu-id="1b4de-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="1b4de-109">請注意，如果您已撰寫封裝，但在 **未安裝** 的語句上執行安裝的條件下，您可能無法移除已公告的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b4de-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="1b4de-110">使用者的電腦上未安裝公告的應用程式，而且安裝程式未設定 [**已安裝**](installed.md) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b4de-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="1b4de-111">必須撰寫封裝，才能卸載公告的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b4de-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 



