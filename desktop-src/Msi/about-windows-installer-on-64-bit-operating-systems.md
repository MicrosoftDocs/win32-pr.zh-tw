---
description: Windows Installer 在使用32位或64位 Windows 的電腦上以服務方式執行。
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: 關於64位作業系統上的 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "104195609"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a><span data-ttu-id="c7b30-103">關於64位作業系統上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c7b30-103">About Windows Installer on 64-Bit Operating Systems</span></span>

<span data-ttu-id="c7b30-104">Windows Installer 在使用32位或64位 Windows 的電腦上以服務方式執行。</span><span class="sxs-lookup"><span data-stu-id="c7b30-104">Windows Installer runs as a service on computers using 32-bit or 64-bit Windows.</span></span> <span data-ttu-id="c7b30-105">2.0 版之前的安裝程式版本只能在32位作業系統上安裝和管理32位 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="c7b30-105">Versions of the installer earlier than version 2.0 can install and manage 32-bit Windows Installer Packages only on 32-bit operating systems.</span></span> <span data-ttu-id="c7b30-106">請注意，您無法在32位作業系統上公告或安裝64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="c7b30-106">Note that you cannot advertise or install a 64-bit application on a 32-bit operating system.</span></span>

<span data-ttu-id="c7b30-107">Windows Installer 封裝必須指定為32位或64位封裝;它不能指定為中性。</span><span class="sxs-lookup"><span data-stu-id="c7b30-107">A Windows Installer package must be specified as either a 32-bit or a 64-bit package; it cannot be specified as neutral.</span></span> <span data-ttu-id="c7b30-108">在使用64位作業系統的電腦上，Windows Installer 服務裝載于64位進程，以安裝32位和64位套件。</span><span class="sxs-lookup"><span data-stu-id="c7b30-108">On a computer using a 64-bit operating system, the Windows Installer service is hosted in a 64-bit process that installs both 32-bit and 64-bit packages.</span></span> <span data-ttu-id="c7b30-109">Windows Installer 在執行64位作業系統的電腦上安裝三種類型的 Windows Installer 套件：</span><span class="sxs-lookup"><span data-stu-id="c7b30-109">Windows Installer installs three types of Windows installer packages on a computer running a 64-bit operating system:</span></span>

-   <span data-ttu-id="c7b30-110">僅包含32位元件的32位封裝。</span><span class="sxs-lookup"><span data-stu-id="c7b30-110">32-bit packages that contain only 32-bit components.</span></span>
-   <span data-ttu-id="c7b30-111">包含一些32位元件的64位套件。</span><span class="sxs-lookup"><span data-stu-id="c7b30-111">64-bit packages containing some 32-bit components.</span></span>
-   <span data-ttu-id="c7b30-112">僅包含64位元件的64位套件。</span><span class="sxs-lookup"><span data-stu-id="c7b30-112">64-bit packages containing only 64-bit components.</span></span>

<span data-ttu-id="c7b30-113">下列各節描述兩種類型的 Windows Installer 封裝和64位封裝的 Windows Installer 所提供的新安裝程式屬性。</span><span class="sxs-lookup"><span data-stu-id="c7b30-113">The follow sections describe the two types of Windows Installer packages and the new installer properties provided by Windows Installer for 64-bit packages.</span></span>

[<span data-ttu-id="c7b30-114">32位 Windows Installer 套件</span><span class="sxs-lookup"><span data-stu-id="c7b30-114">32-bit Windows Installer Packages</span></span>](32-bit-windows-installer-packages.md)

[<span data-ttu-id="c7b30-115">64位 Windows Installer 套件</span><span class="sxs-lookup"><span data-stu-id="c7b30-115">64-bit Windows Installer Packages</span></span>](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a><span data-ttu-id="c7b30-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7b30-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7b30-117">使用64位 Windows Installer 套件</span><span class="sxs-lookup"><span data-stu-id="c7b30-117">Using 64-Bit Windows Installer Packages</span></span>](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



