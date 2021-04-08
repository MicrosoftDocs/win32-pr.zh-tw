---
description: 這份資料是針對正在撰寫自己的安裝程式，以及想要深入瞭解安裝程式資料庫資料表之開發人員的開發人員所設計。 如需安裝程式的一般資訊，請參閱關於 Windows Installer。
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: 資料庫函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691076"
---
# <a name="database-functions"></a>資料庫函數

這份資料是針對正在撰寫自己的安裝程式，以及想要深入瞭解安裝程式資料庫資料表之開發人員的開發人員所設計。 如需安裝程式的一般資訊，請參閱 [關於 Windows Installer](about-windows-installer.md)。

您可以使用安裝程式存取功能來存取資料庫和安裝程式。 這些函式只能由自訂安裝動作和 authoring tools 使用。 部分安裝程式存取函式需要 SQL 查詢字串來查詢資料庫。 查詢必須遵守安裝程式 [SQL 語法](sql-syntax.md)。

本主題依類別列出安裝程式資料庫存取功能。

## <a name="general-database-access-functions"></a>一般資料庫存取函式



| 函式                                                             | 描述                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | 認可對資料庫所做的變更。                                                          |
| [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | 傳回所有主鍵資料行的名稱。                                       |
| [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | 傳回描述資料表狀態的列舉。                                 |
| [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | 準備資料庫查詢並建立 view 物件。                                    |
| [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | 傳回安裝的使用中資料庫。                                       |
| [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | 傳回資料行名稱或定義。                                                    |
| [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | 開啟資料庫檔案以進行資料存取。                                                  |
| [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | 釋放已執行之視圖的結果集。                                           |
| [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | 執行 view 查詢並提供所需的參數。                               |
| [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | 從 view 中提取下一個順序記錄。                                       |
| [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | 傳回在 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 函式中發生的錯誤。 |
| [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | 更新提取的記錄。                                                               |



 

## <a name="database-management-functions"></a>資料庫管理函數



| 函式                                                               | 描述                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | 建立現有轉換的摘要資訊。           |
| [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | 將轉換套用至資料庫。                               |
| [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | 從開啟的資料庫將資料表匯出到文字封存檔案。    |
| [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | 產生兩個資料庫之間差異的轉換檔案。 |
| [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | 將安裝程式的文字封存資料表匯入至開啟的資料庫。   |
| [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | 將兩個資料庫合併在一起。                                   |
| [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | 傳回資料庫的狀態。                               |



 

## <a name="record-processing-functions"></a>記錄處理函式



| 函式                                                 | 描述                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | 使用指定的欄位數目來建立新的記錄物件。      |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | 使用格式字串來格式化記錄欄位資料和屬性。 |
| [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | 將記錄中的所有欄位設定為 null。                            |
| [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | 傳回記錄欄位的長度。                           |
| [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | 傳回記錄中的欄位數。                       |
| [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | 從記錄欄位傳回整數值。                  |
| [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | 傳回記錄欄位的字串值。                     |
| [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | 報告記錄欄位是否為 null。                         |
| [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | 從記錄資料流程欄位將位元組讀入緩衝區。           |
| [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | 將記錄欄位設定為整數位段。                        |
| [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | 從檔案設定記錄資料流程欄位。                         |
| [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | 將字串複製到指定的欄位。                      |



 

## <a name="summary-information-property-functions"></a>摘要資訊屬性函式



| 函式                                                                 | 描述                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | 取得安裝程式資料庫之摘要資訊資料流程的控制碼。    |
| [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | 從摘要資訊取得單一屬性。                   |
| [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | 傳回摘要資訊資料流程中的屬性數目。        |
| [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | 將已變更的摘要資訊寫回摘要資訊串流。 |
| [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | 設定單一摘要資訊屬性。                            |



 

## <a name="installer-state-access-functions"></a>安裝程式狀態存取函式



| 函式                                               | 描述                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | 傳回目前安裝的數位語言。   |
| [**MsiGetLastErrorRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | 傳回上次傳回給呼叫進程的錯誤記錄。 |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | 傳回其中一個布林值內部安裝狀態。    |
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | 取得安裝程式屬性的值。                    |
| [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | 設定安裝屬性的值。                 |
| [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | 設定內部引擎布林狀態。                      |



 

## <a name="installer-action-functions"></a>安裝程式動作函式



| 函式                                             | 描述                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | 執行內建動作、自訂動作或使用者介面 wizard 動作。 |
| [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | 評估包含屬性名稱和值的條件運算式。  |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | 將錯誤記錄傳送至安裝程式進行處理。                    |
| [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | 執行動作順序。                                              |



 

## <a name="installer-location-functions"></a>安裝程式位置函數



| 函式                                     | 描述                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | 傳回目錄資料表中資料夾的完整來源路徑。 |
| [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | 傳回目錄資料表中資料夾的完整目標路徑。 |
| [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | 設定目錄資料表中資料夾的完整目標路徑。    |



 

## <a name="installer-selection-functions"></a>安裝程式選取功能



| 函式                                                     | 描述                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [**MsiEnumComponentCosts**](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | 列舉安裝元件所需的磁碟空間（每個磁片磁碟機）。 |
| [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | 取得元件的狀態。                                    |
| [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | 傳回功能所需的磁碟空間。                        |
| [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | 取得功能的狀態。                                         |
| [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | 傳回有效的安裝狀態。                                  |
| [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | 將元件設定為指定的狀態。                             |
| [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | 在執行時間修改功能的預設屬性。            |
| [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | 將功能設定為指定的狀態。                                 |
| [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | 設定完整產品安裝的安裝層級。          |
| [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | 檢查是否有足夠的磁碟空間。                                    |



 

## <a name="user-interface-functions"></a>消費者介面函式



| 函式                                           | 描述                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | 啟用使用者介面的預覽模式。                             |
| [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | 在顯示的對話方塊中顯示具有主控制項的佈告欄。 |
| [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | 將對話方塊顯示為非模式和非使用中。                         |



 

所有函數都支援 ANSI 和 Unicode 呼叫。 若要使用這些函式，請包含 MsiQuery，並連結至 .Msi。

## <a name="installation-functions"></a>安裝功能

除了上面所列的資料庫存取函式之外，您還可以使用 [安裝程式函數參考](installer-function-reference.md) 一節中所列的安裝程式函數，來建立應用程式的安裝封裝。

 

 



