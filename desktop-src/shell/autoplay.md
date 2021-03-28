---
description: 自動執行時間是 Windows 作業系統的一項功能。
title: 建立啟用自動安裝的 cd-rom 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191188"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="544cc-103">建立啟用自動安裝的 cd-rom 應用程式</span><span class="sxs-lookup"><span data-stu-id="544cc-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="544cc-104">自動執行時間是 Windows 作業系統的一項功能。</span><span class="sxs-lookup"><span data-stu-id="544cc-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="544cc-105">它會將安裝及設定產品的程式自動化，這些產品是在 CD-ROM 上發佈的以 Windows 為基礎的平臺所設計。</span><span class="sxs-lookup"><span data-stu-id="544cc-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="544cc-106">當使用者將已啟用自動安裝的光碟片插入 cd-rom 光碟機時，自動執行會自動執行安裝、設定或執行所選產品的 CD-ROM 上的應用程式。</span><span class="sxs-lookup"><span data-stu-id="544cc-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="544cc-107">自動執行可以用來安裝和執行 CD-ROM 應用程式。</span><span class="sxs-lookup"><span data-stu-id="544cc-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="544cc-108">雖然自動執行最常用於 Windows 應用程式，但是它也可以用來在 Windows Microsoft MS-DOS 會話中安裝、設定或執行以 MS-DOS 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="544cc-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="544cc-109">您可以使用自己的唯一圖示、Config.sys 檔和 Autoexec.bat 檔案，設定每個以 MS-DOS 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="544cc-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="544cc-110">Windows 會為以 MS-DOS 為基礎的應用程式建立正確的設定檔。</span><span class="sxs-lookup"><span data-stu-id="544cc-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="544cc-111">啟動應用程式接著會在視窗中啟動以 ms-dos 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="544cc-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="544cc-112">若要讓執行正常運作，CD-ROM 光碟機必須有32或64位設備磁碟機，以在使用者插入光碟並通知系統時偵測到。</span><span class="sxs-lookup"><span data-stu-id="544cc-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="544cc-113">下列各節將討論如何執行啟用自動安裝的 cd-rom 應用程式。</span><span class="sxs-lookup"><span data-stu-id="544cc-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="544cc-114">建立 AutoRun-Enabled 應用程式</span><span class="sxs-lookup"><span data-stu-id="544cc-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="544cc-115">自動播放 .inf 專案</span><span class="sxs-lookup"><span data-stu-id="544cc-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="544cc-116">啟用和停用自動啟動</span><span class="sxs-lookup"><span data-stu-id="544cc-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



