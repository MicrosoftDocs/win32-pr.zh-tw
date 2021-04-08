---
title: 安裝提供者
description: 安裝 DNS WMI 提供者的程式會根據其安裝所在的 Windows 版本而有所不同。
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- 網域名稱系統、WMI 提供者、安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671964"
---
# <a name="installing-the-provider"></a><span data-ttu-id="068b7-104">安裝提供者</span><span class="sxs-lookup"><span data-stu-id="068b7-104">Installing the Provider</span></span>

<span data-ttu-id="068b7-105">安裝 DNS WMI 提供者的程式會根據其安裝所在的 Windows 版本而有所不同。</span><span class="sxs-lookup"><span data-stu-id="068b7-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="068b7-106">下列程式說明如何在 Windows 2000 上安裝和設定 DNS WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="068b7-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="068b7-107">若要取得 Windows 2000 的 DNS WMI 提供者，請下載下列檔案：</span><span class="sxs-lookup"><span data-stu-id="068b7-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="068b7-108">**警告：** DNS WMI 提供者檔案不可互換。</span><span class="sxs-lookup"><span data-stu-id="068b7-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="068b7-109">Windows 2000 DNS 伺服器需要不同的檔案，以及與 Windows Server 2003 DNS 伺服器不同的程式。</span><span class="sxs-lookup"><span data-stu-id="068b7-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="068b7-110">提供每個的程式。</span><span class="sxs-lookup"><span data-stu-id="068b7-110">The procedure for each is provided.</span></span>

<span data-ttu-id="068b7-111">**在 Windows 2000 伺服器上安裝 DNS WMI 提供者**</span><span class="sxs-lookup"><span data-stu-id="068b7-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="068b7-112">從 Windows 2000 伺服器資源套件取得適用于 Windows 2000 的 DNS WMI 提供者，或從 ftp://ftp.microsoft.com/reskit/win2000/下載檔案（Dnsprov.zip）。</span><span class="sxs-lookup"><span data-stu-id="068b7-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="068b7-113">將 DNS WMI 提供者 (Dnsprov.dll) 和 Dnsschema mof 檔案複製到 <winntdir> \\ system32 \\ wbem 目錄。</span><span class="sxs-lookup"><span data-stu-id="068b7-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="068b7-114">編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="068b7-114">Compile the MOF file.</span></span> <span data-ttu-id="068b7-115">這麼做會自訂符合伺服器的架構。</span><span class="sxs-lookup"><span data-stu-id="068b7-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="068b7-116">**mofcomp.exe dnsschema**</span><span class="sxs-lookup"><span data-stu-id="068b7-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="068b7-117">在 DNS 伺服器上註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="068b7-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="068b7-118">**regsvr32 dnsprov.dll**</span><span class="sxs-lookup"><span data-stu-id="068b7-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="068b7-119">接著，可以使用使用 DNS WMI 提供者來管理 DNS 伺服器的腳本或程式。</span><span class="sxs-lookup"><span data-stu-id="068b7-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="068b7-120">腳本或程式可以從 DNS 伺服器或從用戶端電腦執行。</span><span class="sxs-lookup"><span data-stu-id="068b7-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="068b7-121">執行 DNS WMI 提供者不需要 WMI SDK，但包含許多有用的工具。</span><span class="sxs-lookup"><span data-stu-id="068b7-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="068b7-122">DNS WMI 提供者必須安裝在要管理的任何 DNS 伺服器上;不過，您可以在 DNS 伺服器或遠端主機上執行 DNS 腳本。</span><span class="sxs-lookup"><span data-stu-id="068b7-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="068b7-123">**在 Windows Server 2003 上安裝 DNS WMI 提供者**</span><span class="sxs-lookup"><span data-stu-id="068b7-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="068b7-124">若為 Windows Server 2003 作業系統，系統會自動安裝並註冊 DNS WMI 提供者，並在安裝 DNS 伺服器服務時，編譯其 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="068b7-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




