---
description: 這是每一電腦的系統原則，可在系統管理員只想要安裝每一部電腦的應用程式時使用。
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171c003dbe739c890bf15e5c372e40840fee0aabc9159a837c0b5572a8741b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378511"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

這是每一電腦的 [系統原則](system-policy.md) ，可在系統管理員只想要安裝每一部電腦的應用程式時使用。

如果未設定此原則，安裝程式會依下列順序搜尋應用程式的登錄：管理的應用程式會註冊為每位使用者、每位使用者註冊的非受控應用程式，最後是註冊為每部電腦的應用程式。

如果此原則設定為1，則安裝程式會忽略所有註冊為每個使用者的應用程式，而且只會搜尋以每部電腦方式註冊的應用程式。 Windows Installer 應用程式開發介面或系統的呼叫會忽略每個使用者的應用程式。 嘗試在每個使用者 [安裝內容](installation-context.md) 中執行安裝，會導致安裝程式顯示錯誤訊息並停止安裝。 在此情況下，Windows Installer 也會防止終端機伺服器的每個使用者安裝。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 



