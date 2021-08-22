---
title: 列舉資源
description: 本主題討論用來取得資源清單的函式。
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 6d3fbe60e3013fbeabdb21d74999040b51c42be2a1bb4521cda28a976bfe7aa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034336"
---
# <a name="enumerating-resources"></a>列舉資源

在某些情況下，您可能會想要探索 (PE) 模組的未知可攜式可執行檔的資源內容。 Windows SDK 提供資源列舉函式，可讓您的應用程式取得指定模組中的資源類型、名稱和語言清單。

* [**EnumResourceTypeW**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw)和 [**EnumResourceTypesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw)函式會提供在模組中找到的資源類型清單。
* [**EnumResourceNamesW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw)和 [**EnumResourceNamesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw)函式會提供指定類型內每個資源的名稱。
* [**EnumResourceLanguagesW**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw)和 [**EnumResourceLanguagesExW**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw)函式會提供指定名稱和類型之每個資源的語言。 

這些函式和其相關聯的回呼函式可讓您的應用程式建立模組中所有資源的清單。 這項程式會在 [建立資源清單](using-resources.md)中加以說明。

## <a name="-see-also"></a>-另請參閱

[Msistuff.exe 範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
