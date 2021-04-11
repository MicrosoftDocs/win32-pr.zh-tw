---
description: 當 Windows Installer 處理產品或應用程式安裝的安裝腳本時，它會同時產生復原腳本，並在安裝期間儲存每個已刪除檔案的複本。
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: 復原安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114549"
---
# <a name="rollback-installation"></a><span data-ttu-id="caa65-103">復原安裝</span><span class="sxs-lookup"><span data-stu-id="caa65-103">Rollback Installation</span></span>

<span data-ttu-id="caa65-104">當 Windows Installer 處理產品或應用程式安裝的安裝腳本時，它會同時產生復原腳本，並在安裝期間儲存每個已刪除檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="caa65-104">When the Windows Installer processes the installation script for the installation of a product or application, it simultaneously generates a rollback script and saves a copy of every file deleted during the installation.</span></span> <span data-ttu-id="caa65-105">這些檔案會保存在隱藏的系統目錄中，並在成功完成安裝之後自動刪除。</span><span class="sxs-lookup"><span data-stu-id="caa65-105">These files are kept in a hidden system directory and are automatically deleted once the installation is successfully completed.</span></span> <span data-ttu-id="caa65-106">但是，如果安裝失敗，安裝程式會自動執行復原安裝，將系統復原為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="caa65-106">If however the installation is unsuccessful, the installer automatically performs a rollback installation that returns the system to its original state.</span></span>

<span data-ttu-id="caa65-107">自動復原失敗的安裝是安裝程式的預設行為。</span><span class="sxs-lookup"><span data-stu-id="caa65-107">Automatic rollback of an unsuccessful installation is the default behavior of the installer.</span></span> <span data-ttu-id="caa65-108">若要在安裝期間停用復原，請使用下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="caa65-108">To disable rollback during an installation use one of the following:</span></span>

-   [<span data-ttu-id="caa65-109">**DISABLEROLLBACK 屬性**</span><span class="sxs-lookup"><span data-stu-id="caa65-109">**DISABLEROLLBACK Property**</span></span>](-disablerollback.md)
-   [<span data-ttu-id="caa65-110">**PROMPTROLLBACKCOST 屬性**</span><span class="sxs-lookup"><span data-stu-id="caa65-110">**PROMPTROLLBACKCOST Property**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="caa65-111">DisableRollback 動作</span><span class="sxs-lookup"><span data-stu-id="caa65-111">DisableRollback Action</span></span>](disablerollback-action.md)
-   [<span data-ttu-id="caa65-112">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="caa65-112">DisableRollback</span></span>](disablerollback.md)
-   [<span data-ttu-id="caa65-113">EnableRollback ControlEvent</span><span class="sxs-lookup"><span data-stu-id="caa65-113">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

<span data-ttu-id="caa65-114">一旦停用復原，安裝程式就會設定 [**RollbackDisabled**](rollbackdisabled.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="caa65-114">Whenever rollback is disabled, the installer sets the [**RollbackDisabled**](rollbackdisabled.md) property.</span></span>

<span data-ttu-id="caa65-115">如果安裝使用 [自訂動作](custom-actions.md)，則需要額外撰寫安裝套件才能使用復原功能。</span><span class="sxs-lookup"><span data-stu-id="caa65-115">If an installation uses [custom actions](custom-actions.md), additional authoring of the installation package is required to use rollback functionality.</span></span> <span data-ttu-id="caa65-116">如需詳細資訊，請參閱 [復原自訂動作](rollback-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="caa65-116">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



