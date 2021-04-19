---
description: 成功的安裝程式有兩個階段：取得和執行。 如果安裝失敗，可能會發生復原階段。
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: 安裝機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969237"
---
# <a name="installation-mechanism"></a><span data-ttu-id="d5fde-104">安裝機制</span><span class="sxs-lookup"><span data-stu-id="d5fde-104">Installation Mechanism</span></span>

<span data-ttu-id="d5fde-105">成功的安裝程式有兩個階段：取得和執行。</span><span class="sxs-lookup"><span data-stu-id="d5fde-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="d5fde-106">如果安裝失敗，可能會發生復原階段。</span><span class="sxs-lookup"><span data-stu-id="d5fde-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="d5fde-107">擷取</span><span class="sxs-lookup"><span data-stu-id="d5fde-107">Acquisition</span></span>

<span data-ttu-id="d5fde-108">在取得階段開始時，應用程式或使用者會指示安裝程式安裝功能或應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5fde-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="d5fde-109">然後，安裝程式會執行安裝資料庫之順序資料表中所指定的動作。</span><span class="sxs-lookup"><span data-stu-id="d5fde-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="d5fde-110">這些動作會查詢安裝資料庫，並產生腳本，以提供執行安裝的逐步程式。</span><span class="sxs-lookup"><span data-stu-id="d5fde-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="d5fde-111">執行</span><span class="sxs-lookup"><span data-stu-id="d5fde-111">Execution</span></span>

<span data-ttu-id="d5fde-112">在執行階段中，安裝程式會將資訊以較高的許可權傳遞給處理常式，並執行腳本。</span><span class="sxs-lookup"><span data-stu-id="d5fde-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="d5fde-113">復原</span><span class="sxs-lookup"><span data-stu-id="d5fde-113">Rollback</span></span>

<span data-ttu-id="d5fde-114">如果安裝失敗，安裝程式會還原電腦的原始狀態。</span><span class="sxs-lookup"><span data-stu-id="d5fde-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="d5fde-115">當安裝程式處理安裝腳本時，它會同時產生 rollback 腳本。</span><span class="sxs-lookup"><span data-stu-id="d5fde-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="d5fde-116">除了 rollback 腳本，安裝程式還會在安裝期間儲存其所刪除之每個檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="d5fde-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="d5fde-117">這些檔案會保存在隱藏的系統目錄中。</span><span class="sxs-lookup"><span data-stu-id="d5fde-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="d5fde-118">安裝完成之後，就會刪除復原腳本和儲存的檔案。</span><span class="sxs-lookup"><span data-stu-id="d5fde-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="d5fde-119">如需詳細資訊，請參閱 [復原安裝](rollback-installation.md)。</span><span class="sxs-lookup"><span data-stu-id="d5fde-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



