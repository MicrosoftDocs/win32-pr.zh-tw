---
description: 提供者不需要支援任何部分實例作業。 但是，提供者必須支援部分實例作業的所有語義、處理完整的實例，或傳回 WBEM \_ E \_ 不支援的 \_ 參數。
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: 支援 Partial-Instance 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2043c09ca129acab6976cabda2b854be464d26036cb5b9df1bc5b82989ccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922848"
---
# <a name="supporting-partial-instance-operations"></a>支援 Partial-Instance 作業

提供者不需要支援任何部分實例作業。 但是，提供者必須支援部分實例作業的所有語義、處理完整的實例，或傳回 **WBEM \_ E \_ 不支援的 \_ 參數**。

建立支援部分實例作業的提供者時，您必須遵守下列規則：

-   重複使用 WMI 傳送給提供者的相同內容物件。 WMI 會使用 \_ \_ \_ 名為 value 的 "GET EXT \_ CLIENT \_ REQUEST" 來防止鎖死，並移除此用戶端，然後再將內容物件轉送到提供者。
-   針對不需要部分實例作業的重新進入 WMI，請務必傳回相同的內容物件，而不進行任何修改。 WMI 會接收未 \_ \_ 設定 "GET \_ EXT \_ CLIENT REQUEST" 的內容物件 \_ ，並從內容物件中刪除所有與部分實例作業相關聯的已命名值，再將它傳遞給其他提供者。 不變更內容物件會封鎖其他提供者接收針對不同、不相關的物件所使用的部分實例抓取作業。
-   若要在執行要求時執行可重新進入的部分實例作業，請將遺漏的「 \_ \_ 取得 \_ EXT \_ 用戶端 \_ 要求」命名為 value 和 property clear。 （選擇性）您可以在 \_ \_ \_ \_ 使用可重新進入的呼叫將內容物件傳送回 WMI 之前，修改 "GET EXT properties" 中的屬性（稱為值）。
-   當您在重新進入呼叫期間將內容物件傳回 WMI 時，請勿存取該內容物件;其他提供者可能會在重新進入期間修改屬性清單或其他值。 您只可以在執行的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 呼叫期間檢查或修改內容物件。

 

 



