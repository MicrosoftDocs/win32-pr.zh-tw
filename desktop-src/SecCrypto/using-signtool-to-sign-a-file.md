---
description: 說明如何使用 SignTool 來簽署檔案。
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: 使用 SignTool 來簽署檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114120"
---
# <a name="using-signtool-to-sign-a-file"></a>使用 SignTool 來簽署檔案

下列命令會使用儲存在個人資訊交換 (PFX) 檔中的 [*憑證*](../secgloss/c-gly.md) ，來簽署名為 MyControl.exe 的檔案：

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

下列命令會使用儲存在受密碼保護的 PFX 檔案中的憑證來簽署檔案：

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> 確定您已正確保護密碼。

 

下列命令會簽署檔案並為其加上時間戳記：

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> 如需在檔案已簽署之後，時間戳記檔案的相關資訊，請參閱 [將時間戳記新增至先前簽署](adding-time-stamps-to-previously-signed-files.md)的檔案。

 

下列命令會使用位於「我的存放區」中的憑證來簽署檔案，其主體名稱為「我的公司發行者」：

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

下列命令會簽署 ActiveX 控制項，並提供當系統提示使用者安裝控制項時，Internet Explorer 所顯示的資訊：

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

下列命令會使用憑證（其 [*私密金鑰*](../secgloss/p-gly.md) 資訊受到硬體密碼編譯模組保護）來簽署檔案。 例如，假設名為「我的 High-Value 憑證」的憑證已在硬體密碼編譯模組中安裝私密金鑰，且憑證已正確安裝。

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

下列命令會使用憑證（其 [*私密金鑰*](../secgloss/p-gly.md) 資訊受到硬體密碼編譯模組保護）來簽署檔案。 為 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 存放區指定電腦存放區。

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

下列命令會使用儲存在檔案中的憑證來簽署檔案。 私密金鑰資訊受到硬體密碼編譯模組的保護，且 (CSP) 和 [*金鑰容器*](../secgloss/k-gly.md)的 [*密碼編譯服務提供者*](../secgloss/c-gly.md)是依名稱指定。 如果未正確安裝憑證，此命令會很有用。

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) 會傳回命令列文字，指出簽署作業的結果。 此外，SignTool 會傳回零的結束代碼，表示執行成功，一個用於失敗的執行，另二個則表示執行完成但出現警告。

如需有關驗證檔案簽章的詳細資訊，請參閱 [使用 SignTool 來驗證](using-signtool-to-verify-a-file-signature.md)檔案簽章。 如需有關新增時間戳記的詳細資訊（如果已簽署檔案的話），請參閱 [將時間戳記新增至先前簽署](adding-time-stamps-to-previously-signed-files.md)的檔案。 如需 [SignTool](signtool.md)的詳細資訊，請參閱 [SignTool](signtool.md)。

 

 
