---
title: 伺服器資料物件
description: 伺服器資料物件 (SDO) API 可讓您以程式設計方式設定及管理執行 NPS 的系統。
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d51c4a8b04b9da6994daa4941d255f0d74f68ea858d4a3909ed9ecc1ae28514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128408"
---
# <a name="server-data-objects"></a>伺服器資料物件

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

伺服器資料物件 (SDO) API 可讓您以程式設計方式設定及管理執行 NPS 的系統。 開發人員也可以使用 SDO 來撰寫管理遠端存取原則和設定檔的應用程式。 「路由及遠端存取」服務 (RRAS) 和 NPS 使用遠端存取原則和設定檔，以判斷是否允許遠端用戶端連接到網路存取伺服器 (NAS) 。

SDO API 適用于使用 NPS 或遠端存取原則的任何環境。

使用 SDO API，開發人員可以管理可透過 NPS 使用者介面存取之 NPS 設定的任何元素。

SDO API 也可讓您設定或抓取任何可透過 [使用者撥入設定] 屬性頁存取的值。

SDO API 是由 COM 介面所組成。 SDO API 中的每個介面都繼承自 COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面。 **IDispatch** 介面可讓開發人員從 Visual Basic 或任何 Automation 用戶端，以及從 C/c + + 呼叫 SDO 介面方法。

開發人員也可以從指令碼語言（例如 VBScript）呼叫 SDO API。 不過，因為 VBScript 僅限於使用 VARIANT 類型參數，所以不能使用 SDO 的所有功能。

## <a name="in-this-section"></a>本節內容

[概觀](/windows/desktop/Nps/sdo-about-server-data-objects)

有關伺服器資料物件 API 的一般資訊。

[使用](/windows/desktop/Nps/sdo-using-server-data-objects)

示範如何使用伺服器資料物件 API 的範例程式碼。

[參考](/windows/desktop/Nps/sdo-server-data-objects-reference)

組成伺服器資料物件 API 之列舉型別和介面的檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路原則伺服器 (網際網路驗證服務) ](portal.md)
</dt> <dt>

[遠端存取服務](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 