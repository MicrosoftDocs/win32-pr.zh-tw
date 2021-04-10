---
title: 還原點描述文字
description: 當應用程式呼叫 SRSetRestorePoint 函式時，它可以提供任何文字做為還原點的描述;但是，下表顯示建議的描述文字。
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183607"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="f5d28-103">還原點描述文字</span><span class="sxs-lookup"><span data-stu-id="f5d28-103">Restore Point Description Text</span></span>

<span data-ttu-id="f5d28-104">當應用程式呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 函式時，它可以提供任何文字做為還原點的描述;但是，下表顯示建議的描述文字。</span><span class="sxs-lookup"><span data-stu-id="f5d28-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="f5d28-105">系統修改</span><span class="sxs-lookup"><span data-stu-id="f5d28-105">System modification</span></span>                            | <span data-ttu-id="f5d28-106">還原點類型</span><span class="sxs-lookup"><span data-stu-id="f5d28-106">Restore point type</span></span>      | <span data-ttu-id="f5d28-107">Description</span><span class="sxs-lookup"><span data-stu-id="f5d28-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="f5d28-108">應用程式安裝</span><span class="sxs-lookup"><span data-stu-id="f5d28-108">Application installation</span></span>                       | <span data-ttu-id="f5d28-109">應用程式 \_ 安裝</span><span class="sxs-lookup"><span data-stu-id="f5d28-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="f5d28-110">安裝的 *AppName*</span><span class="sxs-lookup"><span data-stu-id="f5d28-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="f5d28-111"> (新增/移除功能) 的應用程式修改</span><span class="sxs-lookup"><span data-stu-id="f5d28-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="f5d28-112">修改 \_ 設定</span><span class="sxs-lookup"><span data-stu-id="f5d28-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="f5d28-113">設定的 *AppName*</span><span class="sxs-lookup"><span data-stu-id="f5d28-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="f5d28-114">移除應用程式</span><span class="sxs-lookup"><span data-stu-id="f5d28-114">Application removal</span></span>                            | <span data-ttu-id="f5d28-115">應用程式 \_ 卸載</span><span class="sxs-lookup"><span data-stu-id="f5d28-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="f5d28-116">已移除 *AppName*</span><span class="sxs-lookup"><span data-stu-id="f5d28-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="f5d28-117">設備磁碟機安裝</span><span class="sxs-lookup"><span data-stu-id="f5d28-117">Device driver installation</span></span>                     | <span data-ttu-id="f5d28-118">設備 \_ 磁碟機 \_ 安裝</span><span class="sxs-lookup"><span data-stu-id="f5d28-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="f5d28-119">安裝的 *DriverName*</span><span class="sxs-lookup"><span data-stu-id="f5d28-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="f5d28-120">安裝程式（例如 Windows Installer 和 InstallShield）會將這些慣例用於描述文字：</span><span class="sxs-lookup"><span data-stu-id="f5d28-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="f5d28-121">產品名稱後面接著動詞;例如，安裝了 *AppName*。</span><span class="sxs-lookup"><span data-stu-id="f5d28-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="f5d28-122">您可以單獨使用產品名稱 (*appname*) 或產品名稱，也可以使用 (*MyCompany appname*) 的公司名稱。</span><span class="sxs-lookup"><span data-stu-id="f5d28-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




