---
description: Complus 資料表包含安裝 COM + 應用程式所需的資訊。
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Complus 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978386"
---
# <a name="complus-table"></a>Complus 資料表

Complus 資料表包含安裝 COM + 應用程式所需的資訊。

Complus 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 元件\_ | [識別碼](identifier.md) | Y   | N        |
| ExpType     | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件資料表](component-table.md)的第一個資料行中的外部索引鍵。 這是包含 COM + 應用程式的元件。

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

匯出在產生 .msi 檔案期間使用的旗標。 如需詳細資訊，請參閱 Microsoft Windows 軟體開發套件 (SDK) 中的 COM + 檔。

</dd> </dl>

## <a name="remarks"></a>備註

請參閱 [RegisterComPlus 動作](registercomplus-action.md) 和 [UnregisterComPlus 動作](unregistercomplus-action.md)。

請參閱 [安裝具有 Windows Installer 的 COM + 應用程式](installing-a-com--application-with-the-windows-installer.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



