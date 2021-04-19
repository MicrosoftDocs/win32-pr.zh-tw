---
description: Windows Installer 接受統一資源定位器 (URL) 作為安裝的有效來源。
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: 從網際網路下載安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978862"
---
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="fcdc5-103">從網際網路下載安裝</span><span class="sxs-lookup"><span data-stu-id="fcdc5-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="fcdc5-104">Windows Installer 接受統一資源定位器 (URL) 作為安裝的有效來源。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="fcdc5-105">Windows Installer 可以從 URL 位置安裝套件、修補程式和轉換。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="fcdc5-106">如果安裝資料庫位於 URL，則安裝程式會在開始安裝之前將資料庫下載至快取位置。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="fcdc5-107">安裝程式也會從網際網路來源下載適用于使用者選取專案的檔案和封包檔。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="fcdc5-108">如需詳細資訊，請參閱以 [URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md) 。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="fcdc5-109">例如，若要在 web 伺服器上安裝具有來源的封裝 https://server/share/package.msi ，您可以使用 [命令列](command-line-options.md) 選項來安裝封裝和設定 [公用](public-properties.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="fcdc5-110">msiexec/i https://server/share/package.msi *PROPERTY = VALUE*</span><span class="sxs-lookup"><span data-stu-id="fcdc5-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="fcdc5-111">如先前所示的命令列應該傳遞給安裝程式，以從網頁瀏覽器開始安裝。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="fcdc5-112">一般而言，您不應該直接從瀏覽器內按兩下 .msi 檔案，以下載並安裝套件。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="fcdc5-113">這會將 .msi 檔案下載至 [temporary Internet files] 資料夾，並將下列命令傳遞給安裝程式：</span><span class="sxs-lookup"><span data-stu-id="fcdc5-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="fcdc5-114">**msiexec/i c： \\ windows \\ temporary internet files \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="fcdc5-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="fcdc5-115">如果封裝需要任何外部來源檔案或封包，則安裝會失敗，因為這些檔案與 .msi 檔案位於相同的位置。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="fcdc5-116">請注意，因為 [**安裝程式**](installer-object.md) 物件在使用者的電腦上未標示為 [SafeForScripting](safeforscripting.md) ，所以使用者需要調整其瀏覽器的安全性設定，範例才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="fcdc5-117">[**InstallProduct**](installer-installproduct.md)方法可以用來從瀏覽器執行先前的命令，作為按 click 事件。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="fcdc5-118">請注意，由於某些 web 伺服器會區分大小寫，因此 [檔案資料表中的 FileName](file-table.md) 欄位必須完全符合原始程式檔的大小寫，以確保支援網際網路下載。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="fcdc5-119">請參閱 [從網際網路下載並安裝修補程式](downloading-and-installing-a-patch-from-the-internet.md)。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="fcdc5-120">如需保護安裝和使用數位憑證的詳細資訊，請參閱 [撰寫安全安裝](guidelines-for-authoring-secure-installations.md) 和 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)的指導方針。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="fcdc5-121">如需有關如何建立 Windows Installer 套件之 web 安裝的詳細資訊，請參閱 [網際網路下載](internet-download-bootstrapping.md)啟動載入。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="fcdc5-122">可用的網際網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="fcdc5-122">Available Internet Protocols</span></span>

<span data-ttu-id="fcdc5-123">從 Windows Server 2003 和 Windows XP 開始，安裝程式可以使用 HTTP、HTTPS 和檔案通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="fcdc5-124">安裝程式不支援 FTP 和 GOPHER 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="fcdc5-125">Windows Installer 2.0 版可以使用 HTTP、FILE 和 FTP 通訊協定，而且無法使用 HTTPS 和 GOPHER 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fcdc5-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



