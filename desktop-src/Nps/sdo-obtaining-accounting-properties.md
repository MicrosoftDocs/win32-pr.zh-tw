---
title: 取得會計屬性
description: Accounting 物件是要求處理常式集合中的其中一個物件。
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375873"
---
# <a name="obtaining-accounting-properties"></a>取得會計屬性

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

Accounting 物件是要求處理常式集合中的其中一個物件。 要求處理常式集合的列舉值為 **屬性 \_ IAS \_ REQUESTHANDLERS \_ 集合**。 會計物件的處理常式名稱是「Microsoft 帳戶處理」。

下列 Visual Basic 程式碼會從會計物件處理常式存取可用的屬性。


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



若要使用 c + + 存取帳戶處理屬性，請先取得要求處理常式集合。 抓取 [集合](/windows/desktop/Nps/sdo-retrieving-a-collection) 包含的 c + + 程式碼會示範如何取得集合。 要求處理常式集合的列舉值為 **屬性 \_ IAS \_ REQUESTHANDLERS \_ 集合**。  (對應至各種 NPS 集合的值會以 [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) 列舉型別列舉。 ) 

要求處理常式集合包含名為「Microsoft 帳戶處理」的物件。 從集合中取出這個物件。 [從集合中抓取物件](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)的區段包含 c + + 程式碼，該程式碼會示範如何從集合取得物件。

當您擁有 Microsoft Accounting 物件之後，請使用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))取得物件的 [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)介面。 抓取 [使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) 的區段包含 c + + 程式碼，該程式碼會示範如何取得物件的 **ISdo** 介面。 然後，您可以使用 [**ISdo：： GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) 方法來取得 Microsoft Accounting 物件的屬性值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[正在抓取集合](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[從集合中取出物件](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[正在抓取使用者 SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 