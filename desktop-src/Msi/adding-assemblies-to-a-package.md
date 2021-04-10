---
description: Windows Installer 開發人員可以使用本主題中的指導方針來撰寫包含元件的 Windows Installer 套件。
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: 將元件加入封裝中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192471"
---
# <a name="adding-assemblies-to-a-package"></a>將元件加入封裝中

Windows Installer 開發人員可以使用本主題中的指導方針來撰寫包含元件的 Windows Installer 套件。

下列指導方針適用于 Win32 元件，以及 Microsoft .NET Framework 的 common language runtime 所使用的元件。

-   Windows Installer 的元件不能包含一個以上的元件。
-   元件中的所有檔案都應該在單一元件中。
-   包含元件的每個元件都應該在 [MsiAssembly](msiassembly-table.md) 資料表中有一個專案。
-   每個元件的強式組件快取名稱都應該撰寫到 [MsiAssemblyName](msiassemblyname-table.md) 資料表中。
-   當您註冊元件的 COM Interop [時，請使用登錄表，](registry-table.md) 而不是 [類別](class-table.md) 表。
-   具有相同強式名稱的元件是相同的元件。 當不同的應用程式安裝相同的元件時，包含元件的元件應該在其 [元件](component-table.md) 資料表中使用相同的值。

> [!Note]  
> 產品公告可識別可由不同應用程式安裝和使用的元件。 產品公告未識別私用元件。

 

## <a name="adding-win32-assemblies"></a>加入 Win32 元件

當您包含 Win32 元件時，請使用下列指導方針：

-   [元件資料表中](component-table.md)包含 Win32 元件的 KeyPath 值不應為 Null。
-   [元件資料表中](component-table.md)包含 Win32 原則元件的 KeyPath 值應該是資訊清單檔。
-   [元件資料表中](component-table.md)包含 Win32 元件的 KeyPath 值，不是原則元件，不應該是資訊清單檔案或類別目錄檔案。 它應該是元件中的不同檔案。
-   針對 Win32 元件資訊清單的 **assemblyIdentity** 區段中所列的每個名稱和值組，將資料列加入至 [MsiAssemblyName](msiassemblyname-table.md)資料表。

## <a name="adding-assemblies-used-with-the-net-framework"></a>加入與 .NET Framework 搭配使用的元件

當您包含 .NET Framework 的 common language runtime 所使用的元件時，請使用下列指導方針。

-   [元件資料表中](component-table.md)包含元件的 KeyPath 值不應為 Null。
-   當您將 common language runtime 所使用的元件安裝到全域組件快取時，MsiAssembly 資料表的 File Application 資料行中的值 \_ 必須是 Null。
-   針對元件強式名稱的每個屬性，將資料列加入至 [MsiAssemblyName](msiassemblyname-table.md) 資料表。 所有元件都必須有 MsiAssemblyName 資料表中所指定的名稱、版本和文化特性屬性。 全域程式集需要 publicKeyToken 屬性。 下表是通用語言執行平臺使用之通用群組件的 MsiAssemblyName 資料表範例。

[MsiAssemblyName 資料表](msiassemblyname-table.md)



| 元件  | Name           | 值            |
|------------|----------------|------------------|
| ComponentA | Name           | simple           |
| ComponentA | version        | 1.0.0.0          |
| ComponentA | 文化特性        | neutral          |
| ComponentA | publicKeyToken | 9d1ec8380f483f5a |



 

 

 



