---
description: 如果每一電腦的系統原則設定為1，則不能由使用者或系統管理員從電腦移除修補程式。
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5531d5afd7fa98883a3e07dc7c47db625db9051fa223ea7cd6f70e4ceb5aee03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378566"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

如果每一電腦的 [系統原則](system-policy.md) 設定為1，則不能由使用者或系統管理員從電腦移除修補程式。 Windows Installer 仍然可以移除不再適用于產品的修補程式。 如果未設定此原則，只有當使用者已獲得移除修補程式的許可權時，使用者才可以從電腦移除修補程式。 這取決於使用者是否為系統管理員、是否已設定 [DisableMsi](disablemsi.md) 和 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則設定，以及修補程式是否安裝在每個使用者管理、每個使用者的非受控或個別電腦內容中。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



