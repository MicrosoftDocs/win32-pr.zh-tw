---
title: 使用 WMI Windows PowerShell Cmdlet 來管理 BITS Compact Server
description: Windows PowerShell 提供簡單的機制，以連接到遠端電腦上的 Windows Management Instrumentation (WMI) ，以及管理背景智慧型傳送服務 Compact Server (BITS。
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933408"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="9a17a-103">使用 WMI Windows PowerShell Cmdlet 來管理 BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="9a17a-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="9a17a-104">Windows PowerShell 提供簡單的機制，以連接到遠端電腦上的 Windows Management Instrumentation (WMI) ，以及管理背景智慧型傳送服務 Compact Server (BITS。</span><span class="sxs-lookup"><span data-stu-id="9a17a-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="9a17a-105">BITS Compact Server 是選擇性的伺服器元件，必須另外安裝。</span><span class="sxs-lookup"><span data-stu-id="9a17a-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="9a17a-106">如需安裝 Compact Server 的詳細資訊，請參閱 [BITS Compact server](bits-compact-server.md) 檔集。</span><span class="sxs-lookup"><span data-stu-id="9a17a-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="9a17a-107">連接至位提供者。</span><span class="sxs-lookup"><span data-stu-id="9a17a-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="9a17a-108">[Credential 指令程式](/previous-versions//dd315327(v=technet.10))會要求使用者的認證連接到遠端電腦，並將認證指派給 $cred 物件。</span><span class="sxs-lookup"><span data-stu-id="9a17a-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="9a17a-109">[>get-wmiobject](/previous-versions//dd315295(v=technet.10)) Cmdlet 所傳回的物件會指派給 $bcs 變數。</span><span class="sxs-lookup"><span data-stu-id="9a17a-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="9a17a-110">在上述範例中， [>get-wmiobject 指令程式](/previous-versions//dd315295(v=technet.10))會在 Server1 的[](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup)根 \\ Microsoft BITS 命名空間中，取得 BITSCompactServerUrlGroup 類別 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9a17a-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="9a17a-111">[BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup)類別所公開的靜態方法可在 $bcs 物件上呼叫。</span><span class="sxs-lookup"><span data-stu-id="9a17a-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="9a17a-112">如需 BITS 遠端系統管理的詳細資訊，請參閱 [bits 提供者](/previous-versions/windows/desktop/bitsprov/bits-provider) 和 [bits 提供者類別]( /previous-versions//dd904507(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9a17a-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="9a17a-113">使用「音符號」（ (\`) ）來表示分行符號。</span><span class="sxs-lookup"><span data-stu-id="9a17a-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="9a17a-114">在伺服器上建立 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="9a17a-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="9a17a-115">" https://Server1:80/testurlgroup " URL 前置詞字串會指派給 $URLGroup 變數。</span><span class="sxs-lookup"><span data-stu-id="9a17a-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="9a17a-116">$URLGroup 變數會傳遞至 [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) 方法，此方法會在 Server1 上建立 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="9a17a-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="9a17a-117">您可以指定不同的 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="9a17a-117">You can specify a different URL group.</span></span> <span data-ttu-id="9a17a-118">URL 群組必須符合有效的 URL 前置詞字串。</span><span class="sxs-lookup"><span data-stu-id="9a17a-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="9a17a-119">如需 URL 首碼的詳細資訊，請參閱 [UrlPrefix 字串](../http/urlprefix-strings.md)。</span><span class="sxs-lookup"><span data-stu-id="9a17a-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="9a17a-120">在 URL 群組上裝載檔案。</span><span class="sxs-lookup"><span data-stu-id="9a17a-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="9a17a-121">[>get-wmiobject](/previous-versions//dd315295(v=technet.10)) Cmdlet 所傳回的 BITSCompactServerUrlGroup 實例會指派給 $bcsObj 變數。</span><span class="sxs-lookup"><span data-stu-id="9a17a-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="9a17a-122">[CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup)方法是針對具有 "url.txt" URL 尾碼的 $bcsObj、檔案的 "c： \\ \\ temp \\ \\1.txt" 來源路徑，以及空的安全描述項字串做為參數來呼叫。</span><span class="sxs-lookup"><span data-stu-id="9a17a-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="9a17a-123">"url.txt" 尾碼會新增至 URL 群組前置詞。</span><span class="sxs-lookup"><span data-stu-id="9a17a-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="9a17a-124">用戶端可以從下列位址下載檔案： https://Server1:80/testurlgroup/url.txt 。</span><span class="sxs-lookup"><span data-stu-id="9a17a-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="9a17a-125">清除 URL 和 URL 群組。</span><span class="sxs-lookup"><span data-stu-id="9a17a-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="9a17a-126">**System.object Delete** 方法會刪除 $bcsObj 物件。</span><span class="sxs-lookup"><span data-stu-id="9a17a-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a17a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a17a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a17a-128">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="9a17a-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="9a17a-129">位提供者</span><span class="sxs-lookup"><span data-stu-id="9a17a-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="9a17a-130">[位提供者類別]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a17a-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9a17a-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="9a17a-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="9a17a-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="9a17a-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 