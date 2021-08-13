---
description: 如果每一電腦的系統原則設定為 &\# 0034; 1&\# 0034;，安裝程式會防止非系統管理員針對安裝在電腦上的任何應用程式，使用「使用者帳戶控制」 (UAC) 修補。
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821eb480ac09a2fc0416d7b3a54c0df5699a7096b45e56a843afe691886296f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637775"
---
# <a name="disableluapatching"></a>DisableLUAPatching

如果每一電腦的系統原則設定為 "1"，則安裝程式會防止非系統管理員對電腦上安裝的任何應用程式，使用「 [使用者帳戶控制」 (UAC) 修補](user-account-control--uac--patching.md) 。 當每部電腦的系統原則未設定或設定為0時，非系統管理員可以將最低許可權使用者修補程式套用至已啟用最低許可權使用者帳戶修補的應用程式。

使用 [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) 屬性，以防止應用程式的最低許可權修補。

從 Windows Installer 版本3.0 開始，可以使用 DisableLUAPatching 原則。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



