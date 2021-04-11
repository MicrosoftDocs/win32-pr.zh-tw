---
description: 下列章節說明如何使用內建的安裝程式屬性，以及封裝作者所定義的其他屬性。
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: 使用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113244"
---
# <a name="using-properties"></a>使用屬性

下列章節說明如何使用內建的安裝程式屬性，以及封裝作者所定義的其他屬性。 屬性可以是 [公用屬性](public-properties.md) 或 [私用屬性](private-properties.md)。 在初始化安裝程式時需要定義的每個屬性，都必須具有 [屬性工作表](property-table.md)中列出的名稱和初始值。 具有 Null 值的屬性不會列在屬性工作表中。 您可以從程式和自訂動作取得或設定屬性，並從命令列設定公用屬性。 您可以使用條件陳述式中的屬性來修改安裝程式。

[屬性名稱的限制](restrictions-on-property-names.md)

[屬性值的初始化](initialization-of-property-values.md)

[取得和設定屬性](getting-and-setting-properties.md)

[在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)

[使用路徑中的目錄屬性](using-a-directory-property-in-a-path.md)

> [!Note]  
> 請勿將屬性用於密碼或其他必須保持安全的資訊。 安裝程式可能會將撰寫的屬性值寫入至屬性工作表，或在執行時間建立至記錄檔或系統登錄。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性](about-properties.md)
</dt> <dt>

[屬性參考](property-reference.md)
</dt> </dl>

 

 



