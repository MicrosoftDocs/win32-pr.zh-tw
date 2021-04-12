---
title: 應用程式設定
description: 針對單一使用者安裝應用程式，可能會在多使用者遠端桌面服務環境中產生問題。
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316039"
---
# <a name="application-setup"></a><span data-ttu-id="b27c9-103">應用程式設定</span><span class="sxs-lookup"><span data-stu-id="b27c9-103">Application setup</span></span>

<span data-ttu-id="b27c9-104">許多現有應用程式的自動化安裝程式會假設應用程式是針對單一使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="b27c9-104">The automated setup procedure for many existing applications assumes that the application is being installed for a single user.</span></span> <span data-ttu-id="b27c9-105">在多使用者遠端桌面服務環境中，這項假設可能會產生下列問題：</span><span class="sxs-lookup"><span data-stu-id="b27c9-105">In a multiuser Remote Desktop Services environment, this assumption can create the following problems:</span></span>

-   <span data-ttu-id="b27c9-106">如果安裝程式只為一位使用者更新登錄和桌面環境，則其他使用者必須重新安裝整個封裝，否則系統管理員必須手動將資訊從登錄和使用者的桌面複製到其他使用者。</span><span class="sxs-lookup"><span data-stu-id="b27c9-106">If the setup procedure updates the registry and desktop environment for just one user, additional users must reinstall the entire package or an administrator must manually copy information from the registry and desktop of one user to the other users.</span></span>
-   <span data-ttu-id="b27c9-107">透過某些安裝程式，您可以藉由排除功能，在安裝時自訂應用程式。</span><span class="sxs-lookup"><span data-stu-id="b27c9-107">With some setup procedures, you can customize the application at installation time by excluding features.</span></span> <span data-ttu-id="b27c9-108">如果初始安裝程式排除應用程式的一部分，則其他使用者必須重新安裝應用程式，才能取得排除的功能。</span><span class="sxs-lookup"><span data-stu-id="b27c9-108">If the initial installer excludes part of the application, additional users must reinstall the application to get the excluded features.</span></span>

<span data-ttu-id="b27c9-109">若要避免這些問題，安裝程式在遠端桌面工作階段主機 (RD 工作階段主機) server 上安裝應用程式時，應該使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="b27c9-109">To avoid these problems, setup procedures should use the following guidelines when installing an application on a Remote Desktop Session Host (RD Session Host) server:</span></span>

-   <span data-ttu-id="b27c9-110">將應用程式安裝在所有使用者通用的預設使用者環境中。</span><span class="sxs-lookup"><span data-stu-id="b27c9-110">Install applications into the default user environment common to all users.</span></span> <span data-ttu-id="b27c9-111">在安裝應用程式之前，請執行 **change user/install** console 命令，並在安裝完成之後，執行 **change user/execute** console 命令。</span><span class="sxs-lookup"><span data-stu-id="b27c9-111">Before installing the application, execute the **change user /install** console command, and after installation is complete, execute the **change user /execute** console command.</span></span> <span data-ttu-id="b27c9-112">使用遠端桌面服務相容性腳本進行安裝。</span><span class="sxs-lookup"><span data-stu-id="b27c9-112">Use a Remote Desktop Services compatibility script for the installation.</span></span>
-   <span data-ttu-id="b27c9-113">透過使用者設定檔的使用，支援使用者特定的自訂。</span><span class="sxs-lookup"><span data-stu-id="b27c9-113">Support user-specific customization through the use of user profiles.</span></span> <span data-ttu-id="b27c9-114">若要這樣做，請建立系統 [管理範本檔案格式](/previous-versions/windows/desktop/Policy/administrative-template-file-format) ，讓系統管理員可以設定登錄來指出每個使用者可用的功能。</span><span class="sxs-lookup"><span data-stu-id="b27c9-114">To do this, create an [Administrative Template File Format](/previous-versions/windows/desktop/Policy/administrative-template-file-format) so an administrator can configure the registry to indicate the features available to each user.</span></span> <span data-ttu-id="b27c9-115">然後，在執行時間，應用程式可以根據目前使用者的登錄設定中的設定來啟用或停用功能。</span><span class="sxs-lookup"><span data-stu-id="b27c9-115">Then, at run time, the application can enable or disable features depending on the settings in the current user's registry settings.</span></span> <span data-ttu-id="b27c9-116">應用程式可以將每個使用者設定儲存在 **HKEY CURRENT user** 登錄區中，並讓每個使用者根據其喜好設定來設定應用程式。</span><span class="sxs-lookup"><span data-stu-id="b27c9-116">The application can store the per user configuration in the **HKEY CURRENT USER** registry hive and let every user configure the application according to their preferences.</span></span>

 

 