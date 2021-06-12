---
description: 瞭解以字母 R 為開頭的 Windows Installer 概念，例如縮減的 UI 和復原。
ms.assetid: 868cb5b7-d5ab-41c7-a6d4-d7964a8ff6de
title: 'R (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622ddd13bcd0c6ed7969e88eb27d41e281bf2f4
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011271"
---
# <a name="r-windows-installer"></a><span data-ttu-id="15b87-103">R (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="15b87-103">R (Windows Installer)</span></span>

<span data-ttu-id="15b87-104">[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="15b87-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="15b87-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**縮小 UI**</span><span class="sxs-lookup"><span data-stu-id="15b87-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**reduced UI**</span></span>
</dt> <dd>

<span data-ttu-id="15b87-106">安裝程式的 [*內部使用者介面*](i-gly.md) 功能層級。</span><span class="sxs-lookup"><span data-stu-id="15b87-106">Level of the installer's [*internal user interface*](i-gly.md) capabilities.</span></span> <span data-ttu-id="15b87-107">只顯示撰寫的非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="15b87-107">Displays only authored modeless dialog boxes.</span></span> <span data-ttu-id="15b87-108">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="15b87-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

</dd> <dt>

<span data-ttu-id="15b87-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**安裝**</span><span class="sxs-lookup"><span data-stu-id="15b87-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**reinstall**</span></span>
</dt> <dd>

<span data-ttu-id="15b87-110">已安裝應用程式的部分或完全重新安裝。</span><span class="sxs-lookup"><span data-stu-id="15b87-110">Partial or complete reinstallation of an installed application.</span></span> <span data-ttu-id="15b87-111">如果有任何檔案或登錄專案已損毀或遺失，通常會完成修復應用程式。</span><span class="sxs-lookup"><span data-stu-id="15b87-111">Commonly done to repair an application if any files or registry entries have become corrupted or are missing.</span></span> <span data-ttu-id="15b87-112">如需詳細資訊，請參閱 [重新安裝功能或應用程式](reinstalling-a-feature-or-application.md)。</span><span class="sxs-lookup"><span data-stu-id="15b87-112">For more information, see [Reinstalling a Feature or Application](reinstalling-a-feature-or-application.md).</span></span>

</dd> <dt>

<span data-ttu-id="15b87-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**彈性**</span><span class="sxs-lookup"><span data-stu-id="15b87-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**resiliency**</span></span>
</dt> <dd>

<span data-ttu-id="15b87-114">從錯誤中順利復原的應用程式功能，而不會產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="15b87-114">Application capability of graceful recovery from error without generating error messages.</span></span> <span data-ttu-id="15b87-115">如需詳細資訊，請參閱 [復原](resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="15b87-115">For more information, see [Resiliency](resiliency.md).</span></span>

</dd> <dt>

<span data-ttu-id="15b87-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**回 滾**</span><span class="sxs-lookup"><span data-stu-id="15b87-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**rollback**</span></span>
</dt> <dd>

<span data-ttu-id="15b87-117">安裝失敗時，自動還原電腦的原始狀態。</span><span class="sxs-lookup"><span data-stu-id="15b87-117">Automatic restoration of the original state of the computer should the installation fail.</span></span> <span data-ttu-id="15b87-118">如需詳細資訊，請參閱 [復原安裝 (Windows Installer) ](rollback-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="15b87-118">For more information, see [Rollback Installation (Windows Installer)](rollback-installation.md).</span></span>

</dd> </dl>

 

 



