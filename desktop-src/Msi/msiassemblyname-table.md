---
description: MsiAssembly 資料表和 MsiAssemblyName 資料表會指定 common language runtime 元件和 Win32 元件的 Windows Installer 設定。
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: MsiAssemblyName 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997986"
---
# <a name="msiassemblyname-table"></a>MsiAssemblyName 資料表

[MsiAssembly 資料表](msiassembly-table.md)和 MsiAssemblyName 資料表會指定 common language runtime 元件和 Win32 元件的 Windows Installer 設定。 如需詳細資訊，請參閱 [將元件安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md) 和 [Win32 元件的安裝](installation-of-win32-assemblies.md)。

MsiAssemblyName 資料表會針對 .NET Framework 或 Win32 元件的強式組件快取名稱指定元素的架構。 名稱的建立方式是附加具有相同元件索引鍵的所有元素 \_ 。 請參閱下列範例。

Windows Installer 可以將 Win32 元件安裝為 [並存元件](side-by-side-assemblies.md)。 如需詳細資訊，請參閱 [並存元件 API](../sbscs/side-by-side-assembly-api.md)。

MsiAssemblyName 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 元件\_ | [識別碼](identifier.md) | Y   | N        |
| Name        | [Text](text.md)             | Y   | N        |
| 值       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

指定包含此元件之 Windows Installer 元件的 [元件資料表](component-table.md) 中的索引鍵。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

與 [值] 資料行中指定的值相關聯之屬性的名稱。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與 [名稱] 資料行中指定之名稱相關聯的值。

</dd> </dl>

## <a name="remarks"></a>備註

撰寫至 MsiAssemblyName 資料表的資訊必須符合元件的資訊清單檔中的資訊。 如果資訊清單和 MsiAssemblyName 資料表中的資訊不相符，則移除應用程式可能會將元件保留在電腦上。

針對 Win32 元件，[名稱] 欄位中的每個專案都必須在 MsiAssemblyName 資料表中有一個資料列： type、Name、version、language、publicKeyToken 和 processorArchitecture。 您可以在 [值] 欄位中輸入每個名稱的對應值。 MsiAssemblyName 資料表中的名稱/值組必須符合元件資訊清單中的類型、名稱、版本、語言、publicKeyToken 和 processorArchitecture 屬性。

若為私用 common language runtime 元件 ( .NET Frameworkversions 1.0 和 1.1) ，MsiAssemblyName 資料表必須針對 [名稱] 欄位中的每個專案都包含一個資料列： [名稱]、[版本] 和 [文化特性]。 您可以在 [值] 欄位中輸入每個名稱的對應值。

針對全域通用語言執行平臺元件 ( .NET Framework 1.0 和 1.1) 版本，MsiAssemblyName 資料表的 [名稱] 欄位中的每個專案都必須包含一個資料列： [名稱]、[版本]、[文化特性] 和 [PublicKeyToken]。 您可以在 [值] 欄位中輸入每個名稱的對應值。

.NET Framework 版本1.1 是最小版本，可用來執行全域通用語言執行平臺元件的就地更新。 您可以檢查版本的 [**MsiNetAssemblySupport**](msinetassemblysupport.md) 屬性。 MsiAssemblyName 資料表也必須有 FileVersion 欄位，因為這種類型的元件更新只會變更 FileVersion。 如需詳細資訊，請參閱 [更新元件](updating-assemblies.md)。

例如，ComponentA 的組件資訊清單可能會有 Win32 元件的 assemblyIdentity 區段，如下所示。

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

在此情況下，請填入 MsiAssemblyName 資料表，如下所示。



| 元件  | Name                  | 值             |
|------------|-----------------------|-------------------|
| ComponentA | 類型                  | win32             |
| ComponentA | NAME                  | sxstest-簡單 |
| ComponentA | version               | 1.0.0.0           |
| ComponentA | 語言              | en                |
| ComponentA | publicKeyToken        | 1111111111222222  |
| ComponentA | processorArchitecture | x86               |



 

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
