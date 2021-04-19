---
description: IsolatedComponent 資料表的每一筆記錄都會將 [元件應用程式] 資料 (行中指定的元件 \_ 與 [元件共用] 資料行中指定的元件) 產生關聯， \_ (通常是共用的 DLL) 。
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: IsolatedComponent 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970435"
---
# <a name="isolatedcomponent-table"></a>IsolatedComponent 資料表

IsolatedComponent 資料表的每一筆記錄都會將 [元件應用程式] 資料 (行中指定的元件 \_ 與 [元件共用] 資料行中指定的元件) 產生關聯， \_ (通常是共用的 DLL) 。 [IsolateComponents 動作](isolatecomponents-action.md)會將共用的元件複本安裝 \_ 到私人位置，以供元件 \_ 應用程式使用。 這會將元件 \_ 應用程式與其他共用的元件複本隔離，而該元件 \_ 可能會安裝到電腦上的共用位置。 請參閱 [獨立元件](isolated-components.md)。

若要連結一個 \_ 與多個元件 \_ 應用程式共用的元件，請在 IsolatedComponents 資料表中包含每個配對的個別記錄。 安裝程式會將共用的元件檔案複製 \_ 到所安裝之每個元件應用程式的目錄中 \_ 。

IsolatedComponent 資料表具有下列資料行。



| Column                 | 類型                         | 答案 | Nullable |
|------------------------|------------------------------|-----|----------|
| 元件 \_ 共用      | [識別碼](identifier.md) | Y   | N        |
| 元件 \_ 應用程式 | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>元件 \_ 共用
</dt> <dd>

[元件資料表](component-table.md)中的外鍵。 包含共用檔案的元件，通常是 DLL。 DLL 應該是此元件的金鑰檔。 這必須與 [元件應用程式] 資料行中所列的元件不同 \_ 。

共用元件會控制元件之所有隔離複本的註冊，而且必須在元件資料表的 [屬性] 資料行中設定 **msidbComponentAttributesSharedDllRefCount** 旗標。 這樣可確保安裝程式可以管理共用元件的存留期。

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>元件 \_ 應用程式
</dt> <dd>

[元件資料表](component-table.md)中的外鍵。 元件，包含載入共用檔案的 .exe。 .Exe 應該是此元件的金鑰檔。 這必須與元件共用資料行中所列的元件不同 \_ 。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



