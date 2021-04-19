---
description: 您可以使用 Windows Installer 的功能來安裝整個產品。 下列步驟說明如何安裝產品。
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: 安裝應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000314"
---
# <a name="installing-an-application"></a><span data-ttu-id="52b6a-104">安裝應用程式</span><span class="sxs-lookup"><span data-stu-id="52b6a-104">Installing an Application</span></span>

<span data-ttu-id="52b6a-105">您可以使用 Windows Installer 的功能來安裝整個產品。</span><span class="sxs-lookup"><span data-stu-id="52b6a-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="52b6a-106">下列步驟說明如何安裝產品。</span><span class="sxs-lookup"><span data-stu-id="52b6a-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="52b6a-107">**安裝產品**</span><span class="sxs-lookup"><span data-stu-id="52b6a-107">**To install a product**</span></span>

1.  <span data-ttu-id="52b6a-108">藉由呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 函式，透過其安裝或卸載循序執行產品。</span><span class="sxs-lookup"><span data-stu-id="52b6a-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="52b6a-109">藉由呼叫 [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) 函數來指定安裝層級。</span><span class="sxs-lookup"><span data-stu-id="52b6a-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="52b6a-110">您可以使用 [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) 函數的參數來設定安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="52b6a-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="52b6a-111">例如，您可以設定要在本機安裝或從來源安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="52b6a-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="52b6a-112">您可以設定層級來設定要包含的產品功能範圍。</span><span class="sxs-lookup"><span data-stu-id="52b6a-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="52b6a-113">如需安裝應用程式的詳細資訊，請參閱 [復原](resiliency.md) 和 [安裝機制](installation-mechanism.md)。</span><span class="sxs-lookup"><span data-stu-id="52b6a-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 



