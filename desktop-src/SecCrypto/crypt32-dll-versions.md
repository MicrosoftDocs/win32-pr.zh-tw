---
description: Crypt32.dll 是實作為許多 CryptoAPI 函式的模組。
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690139"
---
# <a name="crypt32dll-versions"></a>Crypt32.dll 版本

Crypt32.dll 是在 CryptoAPI 中實作為許多憑證和密碼編譯訊息功能的模組，例如 [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)。 Crypt32.dll 是 Windows 和 Windows Server 作業系統隨附的模組，但此 DLL 的不同版本會提供不同的功能。 沒有 API 可判斷使用中的 CryptoAPI 版本，但是您可以使用 [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) 和 [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) 函式來判斷目前正在使用的 Crypt32.dll 版本。

一般來說，Crypt32.dll 的版本範圍對應至作業系統版本，如下表所示。 不過，此資料表應該僅做為指導方針，因為透過其他更新的方式，Crypt32.dll 版本會與資料表中所示的版本不同。

| Crypt32.dll 版本                               | 作業系統                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *版本* >= 5.131.3790。0                      | Windows Server 2003                                                                                                                                                             |
| *版本* >= 5.131.2600.1243                   | Windows XP Service Pack 2 (SP2) Windows XP Service Pack 1 (SP1) 與[Q329433](https://support.microsoft.com/kb/329433)的修正程式<br/> Windows XP<br/> |
| 5.131.2600.0 <= *version* < 5.131.2600.1243 | 使用 SP1Windows XP 的 Windows XP<br/>                                                                                                                                        |



 

 

 
