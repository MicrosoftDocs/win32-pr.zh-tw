---
description: MsiUnpublishAssemblies 動作會管理要移除之 common language runtime 元件和 Win32 元件的公告。
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: MsiUnpublishAssemblies 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f640338e13f53b115ca3b93aa2a63987efb5aa7cf053d4c8a59d8d20d0f7e3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943895"
---
# <a name="msiunpublishassemblies-action"></a>MsiUnpublishAssemblies 動作

MsiUnpublishAssemblies 動作會管理要移除之 common language runtime 元件和 Win32 元件的公告。 此動作會查詢 [MsiAssembly 資料表](msiassembly-table.md) ，以判斷哪些元件已從全域組件快取中移除已公告或已安裝的功能，以及哪些元件具有已公告或已安裝的父元件，從特定應用程式隔離的位置移除。 如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。

在執行 Windows XP 及更新版本的系統上，Windows Installer 可以安裝 Win32 元件作為[並存元件](side-by-side-assemblies.md)。 如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)。

## <a name="sequence-restrictions"></a>順序限制

MsiUnpublishAssemblies 動作必須位於[InstallExecuteSequence 資料表](installexecutesequence-table.md)中的[InstallInitialize 動作](installinitialize-action.md)之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 應用程式內容。       |
| \[2\] | 元件名稱。             |



 

## <a name="remarks"></a>備註

[MsiPublishAssemblies 動作](msipublishassemblies-action.md)會管理所通告或安裝之元件的公告。

 

 
