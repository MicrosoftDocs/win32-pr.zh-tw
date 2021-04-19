---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS 排序變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4935a6874e28270e73904eb352cd6332e650b7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314951"
---
# <a name="nls-sorting-changes"></a>NLS 排序變更

## <a name="affected-platforms"></a>受影響的平臺

 **客戶** 端-windows XP、windows Vista、windows 7  
**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2  










## <a name="feature-impact"></a>功能影響

 **嚴重性** -高  
**頻率** -低 (少數應用程式受到影響，但如果受到影響，一律會中斷)   


## <a name="description"></a>描述

 (NLS) 函式的國家語言支援可協助應用程式支援世界各地使用者的不同語言和地區設定特定需求。 新的 Windows 版本幾乎都包含 NLS 變更。 此變更會影響定序和排序，因此具有持續性索引的應用程式。

定序資料表有兩個數字，可識別其版本 (修訂) ：已定義的版本和 NLS 版本。 這兩個版本都是 DWORD 值，由主要版本和次要版本所組成。 值的第一個位元組是保留的，接下來的兩個位元組代表主要版本，而最後一個位元組代表次要版本。 以十六進位詞彙來說，此模式為0xRRMMMMmm，其中 R 等於 Reserved、M 等於主要，而 m 等於次要。 例如，次要版本為4的主要版本3會以0x304 表示。

針對主要版本，有一或多個程式碼點變更，讓應用程式必須重新為所有資料重新編制索引，以便讓比較有效。 針對次要版本，不會移動任何專案，但會新增程式碼點。 針對此類型的版本，應用程式只需要使用先前不可排序的值來重新編制字串的索引。 總而言之，與地區設定特定的例外狀況資料表和預設資料表中的資料變更有關，版本號碼的意義如下：

**NLSVersion 主要** –變更「例外狀況」中的程式碼點或地區設定特定的資料表  
**NLSVersion 次要** -在「例外狀況」或地區設定特有的資料表中加入新的程式碼點  
**DefinedVersion 主要** -變更預設表格中的程式碼點  
**DefinedVersion 次要** -在預設資料表中加入新的程式碼點  


**排序發行版本的版本號碼：**



| 作業系統    | 版本           | 版本 (0xRRMMMMmm)          |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/.。。 | N/A-無 GetNLSVersion () API |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>表現

應用程式 (例如資料庫) 具有不檢查 NLS 版本的持續性索引，並在版本變更時重新建立索引，將無法正確排序，或可能無法提供要求的結果。

在使用者介面的案例中，會列出 (例如，字母、數位、英數位元、符號等等) 可能會不正確地排序。

## <a name="solution"></a>解決方法

在 Windows Vista) 之前，您的應用程式可以呼叫 **GetNLSVersionEx** (windows vista 或更新版本) 或 **GetNLSVersion** (，以取得定序資料表的已定義版本和 NLS 版本。

-   GetNLSVersionEx:

*針對名稱所指定的地區設定，取得指定 NLS 功能目前版本的相關資訊*  
此函數可讓 Active Directory 之類的應用程式判斷 NLS 變更是否會影響特定索引資料表所使用的地區設定。 如果沒有，就不需要重新建立資料表的索引。 如需詳細資訊，請參閱處理地區設定和語言資訊。  
此函數支援自訂地區設定。 如果 *lpLocaleName* 指定補充地區設定，則抓取的資料是與該補充地區設定相關聯之定序順序的正確資料。  

**注意：** Windows Vista 之前的 Windows 版本不支援 **GetNLSVersionEx**。  


-   GetNLSVersion (用於 Windows Vista) 之前的 Windows 版本上執行的應用程式：

*針對識別碼指定的地區設定，取得所指定 NLS 功能目前版本的相關資訊*  
此函數可讓 Active Directory 之類的應用程式判斷 NLS 變更是否會影響用於特定索引資料表的地區設定識別碼。 如果沒有，就不需要重新建立資料表的索引。 如需詳細資訊，請參閱處理地區設定和語言資訊。  
**注意：** 此函式只會捕獲識別碼所指定之地區設定的相關資訊。 **GetNLSVersionEx** 函數支援其他地區設定、功能和 RFC 4646 名稱。 不過，Windows Vista 之前的 Windows 版本不支援 **GetNLSVersionEx**。  
只在 Windows Vista 和更新版本上執行的應用程式應該在此函式的喜好設定中使用 **GetNLSVersionEx** 。 **GetNLSVersionEx** 可為補充地區設定提供良好的支援。  


## <a name="compatibility-test"></a>相容性測試

**指示定序版本是否已變更 (也就是您需要重新建立) 索引的步驟：**

-   當您對資料進行原始索引編制時，**請使用 GetNLSVersionEx ()** 取出 **NLSVERSIONINFOEX** 結構。
-   使用您的索引儲存下列屬性來識別版本：  **NLSVERSIONINFOEX. dwNLSVersion** 和 **NLSVERSIONINFOEX. dwDefinedVersion** –這兩個屬性一起指定您要使用的排序表版本。  
    **NLSVERSIONINFOEX. dwEffectiveId** -這會指定排序的有效地區設定。 自訂地區設定會指向內建地區設定的排序。  
    
-   使用索引時， **GetNlsVersionEx ()** 探索您的資料版本。
-   如果三個屬性中的任一個已變更，則您使用的排序資料可能會傳回不同的結果，而且您可能會無法找到記錄的任何索引。
-   如果您知道您的資料不包含不正確 Unicode 程式碼點 (也就是，您的所有字串從對 **IsNLSDefinedString ()**) 的呼叫傳回 **TRUE** ，如果只有 **dwNLSVersion** 和 **dwDefinedVersion** 的低位元組變更 () 以上所述的次要版本，則您可以將它們視為相同。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [Windows 應用程式的國際化](../intl/international-support.md)
-   [GetNLSVersionEx 函式](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion 函式](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [如何判斷定序版本是否已變更](/archive/blogs/shawnste/)

 

 
