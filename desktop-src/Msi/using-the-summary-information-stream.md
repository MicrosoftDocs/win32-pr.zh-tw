---
description: 本節說明 Windows Installer API 中哪些函數可以呼叫摘要資訊資料流程屬性。 如需摘要資訊資料流程及其如何與資料庫搭配運作的詳細資訊，請參閱關於摘要資訊資料流程。
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: 使用摘要資訊資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944294"
---
# <a name="using-the-summary-information-stream"></a>使用摘要資訊資料流程

本節說明 Windows Installer API 中哪些函數可以呼叫摘要資訊資料流程屬性。 如需摘要資訊資料流程及其如何與資料庫搭配運作的詳細資訊，請參閱 [關於摘要資訊資料流程](about-the-summary-information-stream.md)。

-   請務必記住，安裝套裝程式含不同類型的資料庫，而摘要資訊資料流程的某些屬性在不同的資料庫中有不同的意義。 如需詳細資訊，請參閱 [摘要屬性描述](summary-property-descriptions.md)。
-   當資料庫開啟為另一個資料庫的輸出時，輸出資料庫的摘要資訊資料流程實際上是原始資料庫的唯讀鏡像，因此無法變更。 此外，它也不會保存在資料庫中。 若要建立或修改輸出資料庫的摘要資訊，必須將其關閉並重新開啟。

下列步驟說明如何使用摘要資訊資料流程函數：

**使用摘要資訊資料流程屬性**

1.  藉由呼叫 [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) 函式，取得包含摘要資訊資料流程之資料庫的控制碼。
2.  呼叫 [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) 函數來取得現有屬性的數目。
3.  呼叫 [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) 函數來查看單一摘要資訊屬性。
4.  呼叫 [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) 函數來設定單一屬性
5.  呼叫 [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) 函數來儲存摘要資訊屬性。
6.  呼叫 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) 函數，以建立現有轉換的摘要資訊。

[Orca.exe](orca-exe.md) 和 [Msiinfo.exe](msiinfo-exe.md) 是可用於編輯或顯示資料庫之摘要資訊資料流程的工具。 這些工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

您也可以使用 Windows Installer [Automation 介面](automation-interface.md)的下列方法和屬性來存取摘要資訊資料流程。

-   [**SummaryInfo。屬性**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo.PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo。保存**](summaryinfo-persist.md)
-   [**SummaryInformation**](installer-summaryinformation.md)
-   [**SummaryInformation**](database-summaryinformation.md)
-   [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiSumInf.vbs。 此範例腳本可用來管理 Windows Installer 封裝的摘要資訊串流。 如需 WiSumInf.vbs 的詳細資訊，請參閱 [管理摘要資訊](manage-summary-information.md)。

 

 



