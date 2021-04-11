---
description: Microsoft Windows Installer 接受統一資源定位器 (URL) 作為修補程式的有效來源。
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: 從網際網路下載並安裝修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113860"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="564d7-103">從網際網路下載並安裝修補程式</span><span class="sxs-lookup"><span data-stu-id="564d7-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="564d7-104">Microsoft Windows Installer 接受統一資源定位器 (URL) 作為 [修補程式](patch-packages.md)的有效來源。</span><span class="sxs-lookup"><span data-stu-id="564d7-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="564d7-105">若要在上安裝位於 web 伺服器的修補程式 https://MyWeb/MyPatch.msp ，請使用下列命令列：</span><span class="sxs-lookup"><span data-stu-id="564d7-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="564d7-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="564d7-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="564d7-107">若要避免非預期的結果，請按一下網頁上顯示修補檔案 URL 的連結，不要啟動修補程式。</span><span class="sxs-lookup"><span data-stu-id="564d7-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="564d7-108">您也可以使用如下的腳本來安裝修補程式：</span><span class="sxs-lookup"><span data-stu-id="564d7-108">You can also install a patch by using a script like the following:</span></span>


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="564d7-109">請注意，因為 [**安裝程式**](installer-object.md) 物件在使用者的電腦上未標示為 [SafeForScripting](safeforscripting.md) ，所以使用者需要調整其瀏覽器的安全性設定，範例才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="564d7-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="564d7-110">如需詳細資訊，請參閱 [撰寫安全安裝](guidelines-for-authoring-secure-installations.md) 和 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)的指導方針。</span><span class="sxs-lookup"><span data-stu-id="564d7-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="564d7-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="564d7-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564d7-112">修補套件</span><span class="sxs-lookup"><span data-stu-id="564d7-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="564d7-113">建立修補程式套件</span><span class="sxs-lookup"><span data-stu-id="564d7-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="564d7-114">修補自訂應用程式</span><span class="sxs-lookup"><span data-stu-id="564d7-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="564d7-115">從網際網路下載安裝</span><span class="sxs-lookup"><span data-stu-id="564d7-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



