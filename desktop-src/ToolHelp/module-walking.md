---
title: 課程模組
description: 包含指定進程之模組清單的快照集包含指定進程所使用的每個模組、可執行檔或動態連結程式庫 (DLL) 的相關資訊。
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- 動態連結程式庫
- 動態連結程式庫，列舉 Dll
- 列舉
- 列舉，Dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092788"
---
# <a name="module-walking"></a>課程模組

包含指定進程之模組清單的快照集包含指定進程所使用的每個模組、可執行檔或動態連結程式庫 (DLL) 的相關資訊。 您可以使用 [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) 函式來取得清單中第一個模組的資訊。 在取得清單中的第一個模組之後，您可以使用 [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) 函式，在清單中抓取後續模組的資訊。 **Module32First** 和 **Module32Next** 會以模組的相關資訊填入 [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) 結構。

您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)和 [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)的擴充錯誤狀態碼。

> [!Note]  
> 在 [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)的 **th32ModuleID** 成員中指定的模組識別碼，只有在16位的視窗中才有意義。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遍歷模組清單](traversing-the-module-list.md)
</dt> </dl>

 

 