---
description: 您可以使用 Windows Installer 來偵測遺失的元件或檔案，然後重新安裝包含遺漏元件的功能。
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: 安裝遺失的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986884"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="bd682-103">安裝遺失的元件</span><span class="sxs-lookup"><span data-stu-id="bd682-103">Installing a Missing Component</span></span>

<span data-ttu-id="bd682-104">您可以使用 Windows Installer 來偵測遺失的元件或檔案，然後重新安裝包含遺漏元件的功能。</span><span class="sxs-lookup"><span data-stu-id="bd682-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="bd682-105">因為安裝程式會安裝功能，而不是元件，所以必須先解析遺失檔案所屬的元件，然後再安裝包含該元件的功能。</span><span class="sxs-lookup"><span data-stu-id="bd682-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="bd682-106">如果有一個以上的功能連結至元件，安裝程式會安裝需要最少磁碟空間的功能。</span><span class="sxs-lookup"><span data-stu-id="bd682-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="bd682-107">如果您呼叫 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)，您可以確認元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="bd682-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="bd682-108">不過，仍有可能遺失屬於元件的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="bd682-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="bd682-109">在該案例中，請呼叫 [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)。</span><span class="sxs-lookup"><span data-stu-id="bd682-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="bd682-110">然後，安裝程式會解析為檔案所屬的元件，並安裝連結到需要最少磁碟空間之元件的功能。</span><span class="sxs-lookup"><span data-stu-id="bd682-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="bd682-111">如果 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 函式意外失敗，您必須安裝任何遺失的元件。</span><span class="sxs-lookup"><span data-stu-id="bd682-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="bd682-112">下列程式說明如何安裝遺失的元件。</span><span class="sxs-lookup"><span data-stu-id="bd682-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="bd682-113">**偵測並安裝遺失的元件**</span><span class="sxs-lookup"><span data-stu-id="bd682-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="bd682-114">呼叫 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 來確認元件的金鑰檔是否存在。</span><span class="sxs-lookup"><span data-stu-id="bd682-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="bd682-115">但是，即使元件的金鑰檔存在，仍然可能遺失屬於元件的其他檔案。</span><span class="sxs-lookup"><span data-stu-id="bd682-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="bd682-116">如果與元件相關聯的功能未知，則呼叫 [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) 函數。</span><span class="sxs-lookup"><span data-stu-id="bd682-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="bd682-117">如果已知與元件相關聯的功能，請呼叫 [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) 或 [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) 函數。</span><span class="sxs-lookup"><span data-stu-id="bd682-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="bd682-118">如果應用程式無法開啟檔案，請呼叫 [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) 。</span><span class="sxs-lookup"><span data-stu-id="bd682-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



