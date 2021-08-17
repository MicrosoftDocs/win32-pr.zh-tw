---
description: 如果每一電腦的系統原則設定為 &\# 0034; 1&\# 0034;，則安裝程式在網頁中的腳本使用安裝程式的自動化介面時，不會提示使用者。
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9a78bded284a687994075fdda1276122df2ab68716c4aaf759b4f5750aeb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990148"
---
# <a name="safeforscripting"></a>SafeForScripting

如果每一電腦的 [系統原則](system-policy.md) 設定為 "1"，則安裝程式在網頁中的腳本使用安裝程式的 [自動化介面](automation-interface.md)時，不會提示使用者。

在設定此原則之前，您應該考慮上述使用者提示是否為使用者提供適當的安全性層級。 如果未設定此原則，當網際網路瀏覽器裝載的腳本嘗試安裝應用程式時，系統會警告使用者，並要求他們接受或拒絕安裝。 設定 SafeForScripting 會抑制此警告，而且可能會允許在系統上安裝應用程式，而不需要使用者的知識。 此原則可能適用于使用 web 型工具來散發程式的企業。

如需詳細資訊，請參閱[撰寫安全安裝](guidelines-for-authoring-secure-installations.md)和[數位簽章](digital-signatures-and-windows-installer.md)的指導方針，以及[從網際網路下載安裝](downloading-an-installation-from-the-internet.md)的 Windows Installer 和下載。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 



