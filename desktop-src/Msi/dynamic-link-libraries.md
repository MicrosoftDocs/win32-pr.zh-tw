---
description: 自訂動作可以呼叫動態連結程式庫中所定義的函式， (DLL) 以 C 或 c + + 撰寫。
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: 'Dynamic-Link 程式庫 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026879"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Dynamic-Link 程式庫 (Windows Installer) 

自訂動作可以呼叫動態連結程式庫中所定義的函式， (DLL) 以 C 或 c + + 撰寫。 DLL 可以是在目前安裝期間安裝的檔案，或是源自于安裝資料庫之 [二進位資料表](binary-table.md) 的暫存二進位資料流程。

請注意，任何已呼叫的函式（包括 Dll 中的自訂動作）都必須指定 \_ \_ stdcall 呼叫慣例。 例如，若要呼叫 CustomAction，請使用下列程式。


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



如需詳細資訊，請參閱[從自訂動作內部存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)。

下列自訂動作類型會呼叫動態連結程式庫。



| 自訂動作類型                                 | Description                               |
|----------------------------------------------------|-------------------------------------------|
| [自訂動作類型1](custom-action-type-1.md)   | 儲存在二進位資料表資料流程中的 DLL 檔案。 |
| [自訂動作類型17](custom-action-type-17.md) | 與產品一起安裝的 DLL 檔案。        |



 

> [!Note]  
> 若要使用 COM，您需要在自訂動作中呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 。 如果您發現執行緒已經初始化，請勿退出。 例如，執行緒會在個別電腦安裝中初始化，但不會在每個使用者安裝中初始化。

 

請參閱 [所有自訂動作類型的摘要清單](summary-list-of-all-custom-action-types.md) ，以取得所有自訂動作類型的摘要，以及它們如何編碼至 [CustomAction 資料表](customaction-table.md)。

 

 
