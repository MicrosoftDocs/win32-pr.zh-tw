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
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>使用 WMI Windows PowerShell Cmdlet 來管理 BITS Compact Server

Windows PowerShell 提供簡單的機制，以連接到遠端電腦上的 Windows Management Instrumentation (WMI) ，以及管理背景智慧型傳送服務 Compact Server (BITS。 BITS Compact Server 是選擇性的伺服器元件，必須另外安裝。 如需安裝 Compact Server 的詳細資訊，請參閱 [BITS Compact server](bits-compact-server.md) 檔集。

1.  連接至位提供者。

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    [Credential 指令程式](/previous-versions//dd315327(v=technet.10))會要求使用者的認證連接到遠端電腦，並將認證指派給 $cred 物件。

    [>get-wmiobject](/previous-versions//dd315295(v=technet.10)) Cmdlet 所傳回的物件會指派給 $bcs 變數。 在上述範例中， [>get-wmiobject 指令程式](/previous-versions//dd315295(v=technet.10))會在 Server1 的[](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup)根 \\ Microsoft BITS 命名空間中，取得 BITSCompactServerUrlGroup 類別 \\ 。 [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup)類別所公開的靜態方法可在 $bcs 物件上呼叫。 如需 BITS 遠端系統管理的詳細資訊，請參閱 [bits 提供者](/previous-versions/windows/desktop/bitsprov/bits-provider) 和 [bits 提供者類別]( /previous-versions//dd904507(v=vs.85))。

    > [!Note]  
    > 使用「音符號」（ (\`) ）來表示分行符號。

     

2.  在伺服器上建立 URL 群組。

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    " https://Server1:80/testurlgroup " URL 前置詞字串會指派給 $URLGroup 變數。 $URLGroup 變數會傳遞至 [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) 方法，此方法會在 Server1 上建立 URL 群組。

    您可以指定不同的 URL 群組。 URL 群組必須符合有效的 URL 前置詞字串。 如需 URL 首碼的詳細資訊，請參閱 [UrlPrefix 字串](../http/urlprefix-strings.md)。

3.  在 URL 群組上裝載檔案。

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    [>get-wmiobject](/previous-versions//dd315295(v=technet.10)) Cmdlet 所傳回的 BITSCompactServerUrlGroup 實例會指派給 $bcsObj 變數。 [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup)方法是針對具有 "url.txt" URL 尾碼的 $bcsObj、檔案的 "c： \\ \\ temp \\ \\1.txt" 來源路徑，以及空的安全描述項字串做為參數來呼叫。 "url.txt" 尾碼會新增至 URL 群組前置詞。 用戶端可以從下列位址下載檔案： https://Server1:80/testurlgroup/url.txt 。

4.  清除 URL 和 URL 群組。

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    **System.object Delete** 方法會刪除 $bcsObj 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[BITS Compact Server](./bits-compact-server.md)
</dt> <dt>

[位提供者](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[位提供者類別]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 