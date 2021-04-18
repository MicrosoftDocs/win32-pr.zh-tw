---
description: 適當授權的用戶端會使用 ICertView 介面來查看憑證服務資料庫。
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: 查看憑證服務資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115608"
---
# <a name="viewing-the-certificate-services-database"></a>查看憑證服務資料庫

適當授權的用戶端會使用 [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) 介面來查看憑證服務資料庫。 請注意，在隨附的產品中，憑證授權單位單位 MMC 嵌入式管理單元可以用來查看憑證服務資料庫。 [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) 是提供來以程式設計方式查看資料庫。 從 Windows XP 開始支援 **ICertView** 介面。

經適當授權的用戶端是指已被授與許可權來查看憑證服務資料庫的使用者;您可以使用「憑證授權單位單位」 MMC 嵌入式管理單元來授與或限制存取權，以在 [*憑證授權單位*](../secgloss/c-gly.md)單位的 [內容 **] 下查看** 資料庫 (，請按一下 [**安全性**] 索引標籤) 。 此外，若要使用 [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) 物件，用戶端工作站必須已安裝憑證服務用戶端元件。

雖然使用 [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) 及其相關介面的案例有很多種，但以下說明了一個可能的順序，可根據 **ICertView** 來開發用戶端應用程式：

**若要查看憑證服務資料庫**

1.  取得 [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) 物件的實例之後，請呼叫 [**ICertView：： OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) ，以與特定電腦上的 [*憑證授權單位*](../secgloss/c-gly.md) 單位進行通訊。
2.  呼叫 [**ICertView：： SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) 來指定 view 中的資料行數目;此呼叫也用來指定預設的視圖。 如果未在呼叫中指定預設視圖，則呼叫端必須針對要包含在視圖中的每個資料行呼叫 [**ICertView：： SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) 。
3.  選擇性。 藉由呼叫 [**ICertView：： SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) 函數，指定資料庫查詢的排序準則和/或限定準則。 符合條件的條件包括：告知視圖要根據限定詞（例如大於、小於、等於等）來取出資料。
4.  呼叫 [**ICertView：： OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) 以取出 view 中的資料;此視圖的資料將由 [**ICertView：： SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (所要求的資料行所組成，而且如果未指定預設 View， [**ICertView：： SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)) 。 如果呼叫 [**ICertView：： SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) ，資料行中的資料將會排序及/或限定。 **ICertView：： OpenView** 會建立 [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) 物件，可用來列舉視圖的資料列。
5.  使用 [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) 方法 [**IEnumCERTVIEWROW：： EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute)、 [**IEnumCERTVIEWROW：： EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)和 [**IEnumCERTVIEWROW：： EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) ，視需要取出屬性、資料行和延伸資料。

 

 
