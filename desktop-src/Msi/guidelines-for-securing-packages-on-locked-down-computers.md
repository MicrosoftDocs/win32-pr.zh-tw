---
description: 若要在鎖定的電腦上維護安全的軟體安裝，請在撰寫 Windows Installer 套件時遵守這些指導方針。
ms.assetid: 46ee99a9-b77d-4138-98f0-04428e68cf30
title: 保護鎖定電腦上的套件安全
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8380ad7e342d35bff80da4d4d86c37759a80a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850199"
---
# <a name="securing-packages-on-locked-down-computers"></a><span data-ttu-id="b3db1-103">保護鎖定電腦上的套件安全</span><span class="sxs-lookup"><span data-stu-id="b3db1-103">Securing Packages on Locked-Down Computers</span></span>

<span data-ttu-id="b3db1-104">在撰寫將用於鎖定電腦的 Windows Installer 套件時遵循下列指導方針，有助於在安裝期間維護安全的環境：</span><span class="sxs-lookup"><span data-stu-id="b3db1-104">Adherence to the following guidelines when authoring a Windows Installer package that will be used on locked-down computers helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="b3db1-105">測試套件是否與 Windows Installer 的電腦 [系統原則](system-policy.md)相容。</span><span class="sxs-lookup"><span data-stu-id="b3db1-105">Test your package for compatibility with the Windows Installer machine [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="b3db1-106">請確定您已使用所有 [使用者介面層級](user-interface-levels.md)、無、基本、受限和完整封裝執行。</span><span class="sxs-lookup"><span data-stu-id="b3db1-106">Make sure you package runs with all [user interface levels](user-interface-levels.md), none, basic, limited, and full.</span></span>
-   <span data-ttu-id="b3db1-107">在 NTFS 磁碟分割上測試您的封裝，並以更 [*高*](e-gly.md) 和非提高許可權來進行。</span><span class="sxs-lookup"><span data-stu-id="b3db1-107">Test your package on NTFS partitions, both with [*elevated*](e-gly.md) and non-elevated privileges.</span></span>
-   <span data-ttu-id="b3db1-108">從 Windows Installer 3.0 開始， [ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md) 可讓非系統管理員使用者修補個別電腦內容中安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b3db1-108">Starting with Windows Installer 3.0, [User Account Control (UAC) Patching](user-account-control--uac--patching.md) enables non-administrator users to patch applications installed in the per-machine context.</span></span> <span data-ttu-id="b3db1-109">在 Windows Vista 和 Windows XP 上測試修補套件，以供具有系統管理員存取權的使用者和非系統管理員的使用者進行安裝。</span><span class="sxs-lookup"><span data-stu-id="b3db1-109">Test your patch package on Windows Vista and Windows XP for both installation by users with administrator access and by non-administrator users.</span></span>

 

 



