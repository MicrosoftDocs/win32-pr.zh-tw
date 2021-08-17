---
description: Microsoft Windows HTTP 服務 (WinHTTP) 憑證設定工具 &\# 0034; WinHttpCertCfg.exe&\# 0034;，可讓系統管理員在任何憑證存放區中安裝和設定用戶端憑證，該憑證存放區可由網際網路伺服器 Web 應用程式管理員 (IWAM) 帳戶存取。 此工具也可讓您不需要對帳戶（例如 IWAM 帳戶）採取任何特殊動作，就能在使用 Active Server Pages (ASP) 時取得憑證的存取權。
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe，憑證設定工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ce9978f6e2ffcafa1357a45dbeff80c12bf0e6ea2f7f3fb9656376b33dfb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743796"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe，憑證設定工具

[Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md)憑證設定工具「WinHttpCertCfg.exe」，可讓系統管理員在任何憑證存放區中安裝和設定用戶端憑證，該 [*憑證存放區*](glossary.md)可由網際網路伺服器 Web 應用程式管理員 (IWAM) 帳戶存取。 此工具也可讓您不需要對帳戶（例如 IWAM 帳戶）採取任何特殊動作，就能在使用 Active Server Pages (ASP) 時取得憑證的存取權。

Microsoft Management Console (MMC) 可讓系統管理員將用戶端憑證匯入本機電腦。 不過，匯入憑證並不會自動授與其他帳戶私密金鑰的存取權。 此私密金鑰是用戶端憑證驗證的必要項。 Microsoft Windows HTTP 服務 (WinHTTP) 憑證設定工具，可在必要時，將存取權授與其他帳戶，例如 IWAM 帳戶。

-   [使用憑證設定工具](#using-the-certificate-configuration-tool)
-   [範例](#examples)

## <a name="using-the-certificate-configuration-tool"></a>使用憑證設定工具

WinHttpCertCfg.exe 的 WinHTTP 憑證設定工具，可從[Windows Server 2003 資源套件工具](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd)網站下載。 下列範例程式碼顯示要搭配此工具使用的有效命令列參數。

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

下表列出設定工具的參數。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>參數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>顯示語法資料。</td>
</tr>
<tr class="even">
<td>-i</td>
<td>指定要從個人資訊匯入憑證 Exchange (PFX) 檔。 此參數後面必須接著檔案的名稱。 當指定這個參數時， &quot; &quot; &quot; 也必須指定-a 和-c &quot; 。</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>指定授與私密金鑰的存取權。 當指定這個參數時， &quot; &quot; &quot; 也必須指定-a、-c &quot; 和 &quot; -s &quot; 。</td>
</tr>
<tr class="even">
<td>-r</td>
<td>指定移除私密金鑰的存取權。 當指定這個參數時， &quot; &quot; &quot; 也必須指定-a、-c &quot; 和 &quot; -s &quot; 。</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>指定列出具有私密金鑰存取權的帳戶。 當指定這個參數時， &quot; &quot; &quot; 也必須指定-c 和-s &quot; 。</td>
</tr>
<tr class="even">
<td>-a</td>
<td>指定要設定之電腦上的使用者帳戶。 這可以是本機電腦或網域帳戶，例如 &quot; IWAM_TESTMACHINE &quot; 、 &quot; TESTUSER &quot; 或 &quot; TESTDOMAIN\DOMAINUSER &quot; 。</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>指定 <a href="glossary.md"><em>憑證存放區</em></a>的位置和名稱。 使用 &quot; LOCAL_MACHINE &quot; 或 &quot; CURRENT_USER &quot; 指定要用於位置的登錄分支。 <em>憑證存放區</em>可以是電腦上安裝的任何一個。 一般名稱範例包括 &quot; MY &quot; 、 &quot; Root &quot; 和 &quot; TrustedPeople &quot; 。 <em>憑證存放區</em>的位置和名稱會以反斜線分隔，例如 &quot; LOCAL_MACHINE \root &quot; 。
<blockquote>
[!Note]<br />
雖然您 &quot; &quot; 可以使用這個參數來指定登錄的 CURRENT_USER 分支，但延伸私密金鑰的存取主要是用於安裝在本機電腦 <a href="glossary.md"><em>憑證存放區</em></a> 中的憑證，可供多位使用者存取。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>指定不區分大小寫的搜尋字串，以尋找包含此子字串的主體名稱的第一個列舉憑證。</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>指定用來匯入憑證和私密金鑰的密碼。 這只會與匯入選項搭配使用。</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> 使用者必須有足夠的許可權才能使用此工具，這需要使用者是系統管理員，以及安裝用戶端憑證的相同使用者（如果有安裝的話）。
>
> 「WinHttpCertCfg.exe」工具不適用於設定儲存在檔案系統（例如 FAT32）中的憑證，這種方法不支援 (ACL) 的存取控制清單。

## <a name="examples"></a>範例

下列範例顯示可使用設定工具的一些方式。

1.  此命令會列出在登錄本機電腦分支的「根」 [*憑證存放區*](glossary.md) 中，可存取 "MyCertificate" 憑證之私密金鑰的帳戶 \_ 。

    **winHTTPcertcfg.exe-l-c 本機 \_ 電腦 \\ 根目錄-s MyCertificate**

2.  此命令會在 TESTUSER 帳戶的 "My" [*憑證存放區*](glossary.md) 中，授與 "MyCertificate" 憑證私密金鑰的存取權。

    **winHTTPcertcfg.exe-g-c 本機 \_ 電腦 \\ My-s MyCertificate-a TESTUSER**

3.  此命令會從 PFX 檔案匯入憑證和私密金鑰，並將私密金鑰存取權延伸至另一個帳戶。

    **winHTTPcertcfg.exe-i PFXFile-c LOCAL \_ MACHINE \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**

4.  此命令會針對 \_ 具有指定憑證的 IWAM TESTMACHINE 帳戶拒絕存取私密金鑰。

    **winHTTPcertcfg.exe-r-c 本機 \_ 電腦 \\ 根目錄-s MYCERTIFICATE-IWAM \_ TESTMACHINE**

 

 




