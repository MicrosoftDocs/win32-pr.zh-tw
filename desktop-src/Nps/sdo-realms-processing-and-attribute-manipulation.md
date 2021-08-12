---
title: 領域處理和屬性操作
description: 領域處理（也稱為屬性操作）是指將要求存取權的使用者名稱轉換。
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8054ad8234ca4772a52619d83bc85a9d357f2cf8da2f1c969eed918c75a8305a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618944"
---
# <a name="realms-processing-and-attribute-manipulation"></a>領域處理和屬性操作

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

領域處理（也稱為屬性操作）是指將要求存取權的使用者名稱轉換。 也可以操作呼叫端識別碼和被呼叫的工作站識別碼。 領域處理規則是 Proxy 配置檔案屬性集合的一部分。

針對每個操作，您需要建立兩個 [操作規則](/windows/desktop/Nps/sdo-manipulation-rule) 屬性。 每個屬性都是一個字串值。 第一個規則包含表示要比對之模式的正則運算式。 第二個規則包含表示取代文字的正則運算式。 您也必須建立 [操作目標](/windows/desktop/Nps/sdo-manipulation-target) 屬性。 這個屬性是一個列舉，可指定要操作的使用者資訊部分。

建立屬性的順序很重要。 NPS 會依照這些屬性的建立順序來處理它們。

下表顯示一組操作屬性的範例。



| 名稱                 | 類型         | 字串值     |
|----------------------|--------------|------------------|
| msManipulationRule   | **VT \_ BSTR** | "@company.com"   |
| msManipulationRule   | **VT \_ BSTR** | "@microsoft.com" |
| msManipulationRule   | **VT \_ BSTR** | "^.+@"           |
| msManipulationRule   | **VT \_ BSTR** | "guest@"         |
| msManipulationTarget | **VT \_ I4**   | 「1」              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件模型階層](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[SDO 支援的屬性](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[建立連接要求原則](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 