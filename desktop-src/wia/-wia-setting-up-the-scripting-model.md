---
description: 若要使用 Windows 映像取得 (WIA) 腳本模型，您必須在電腦上安裝並註冊檔案 Wiascr.dll。
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: 設定腳本模型開發環境
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191391"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="a1276-103">設定腳本模型開發環境</span><span class="sxs-lookup"><span data-stu-id="a1276-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="a1276-104">若要使用 Windows 映像取得 (WIA) 腳本模型，您必須在電腦上安裝並註冊檔案 Wiascr.dll。</span><span class="sxs-lookup"><span data-stu-id="a1276-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="a1276-105">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="a1276-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="a1276-106">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="a1276-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="a1276-107">將此檔案從 WIA SDK 複製到 *% windir%*/System32 (例如，c： \\ windows \\ System32) 目錄。</span><span class="sxs-lookup"><span data-stu-id="a1276-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="a1276-108">在命令列中，流覽至此目錄，然後輸入 **regsvr32 Wiascr.dll**。</span><span class="sxs-lookup"><span data-stu-id="a1276-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="a1276-109">這會在系統登錄中輸入必要的資訊。</span><span class="sxs-lookup"><span data-stu-id="a1276-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="a1276-110">您現在已準備好使用 WIA 腳本模型。</span><span class="sxs-lookup"><span data-stu-id="a1276-110">You are now ready to use the WIA scripting model.</span></span>

 

 
