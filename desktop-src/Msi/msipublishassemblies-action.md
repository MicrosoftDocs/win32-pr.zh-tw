---
description: MsiPublishAssemblies 動作會管理 common language runtime 元件和 Win32 元件的公告。
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: MsiPublishAssemblies 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524175a957249a48f7c72409ad7b4c55b31f642753db11875a9567ef35a2acf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804188"
---
# <a name="msipublishassemblies-action"></a>MsiPublishAssemblies 動作

MsiPublishAssemblies 動作會管理 common language runtime 元件和 Win32 元件的公告。 此動作會查詢 [MsiAssembly 資料表](msiassembly-table.md) ，以判斷哪些元件具有要在全域組件快取中通告或安裝的功能，以及哪些元件有父元件要被通告或安裝到特定應用程式的隔離位置。 如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。

在 Microsoft Windows XP 及更新版本的系統上，Windows Installer 可以安裝 Win32 元件作為[並存元件](side-by-side-assemblies.md)。 如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)。

## <a name="sequence-restrictions"></a>順序限制

MsiPublishAssemblies 動作必須位於[InstallExecuteSequence 資料表](installexecutesequence-table.md)或[AdvtExecuteSequence 資料表](advtexecutesequence-table.md)中的[InstallInitialize 動作](installinitialize-action.md)之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 應用程式內容。       |
| \[2\] | 元件名稱。             |



 

## <a name="remarks"></a>備註

如需詳細資訊，請參閱 [元件](assemblies.md)。

[MsiUnpublishAssemblies 動作](msiunpublishassemblies-action.md)會管理要移除之元件的公告。

 

 
