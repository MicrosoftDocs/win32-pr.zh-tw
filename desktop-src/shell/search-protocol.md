---
description: 搜尋：應用程式通訊協定是一種可延伸的慣例，可在 Windows Vista Service Pack 1 (SP1) 和更新版本上呼叫桌面搜尋應用程式。
title: 使用搜尋通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991738"
---
# <a name="using-the-search-protocol"></a>使用搜尋通訊協定

**搜尋：** [應用程式通訊協定](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85))是一種可延伸的慣例，可在 Windows Vista SERVICE Pack 1 (SP1) 和更新版本上呼叫桌面搜尋應用程式。 此通訊協定是在 Windows Vista SP1 (中建立的，如需詳細資訊，請參閱知識庫檔中 windows vista [desktop search 的 windows Vista Service Pack 1 變更（Windows Vista Service Pack 1 中的 Windows vista desktop Search 變更](https://support.microsoft.com/kb/941946) ）) ，讓 Windows 能夠判斷和呼叫預設桌面搜尋應用程式。

通訊協定語法提供許多參數，可用於執行常見的桌面搜尋，例如使用者輸入的搜尋字詞或搜尋開始的位置。 當使用者從兩個可用的搜尋專案點之一搜尋 ([ **開始** ] 功能表或 Windows 檔案總管) 時，作業系統會使用搜尋通訊協定來啟動預設的桌面搜尋應用程式。 其執行方式是將使用者輸入的搜尋詞彙新增至標準搜尋通訊協定語法，並將該資訊傳遞給註冊為預設搜尋應用程式的應用程式。

如果未安裝其他桌面搜尋應用程式，則在這些進入點中輸入的搜尋會啟動 Windows Search Explorer。 但是，協力廠商開發人員可以建立、安裝及註冊其應用程式，以處理搜尋通訊協定，並作為預設搜尋應用程式。 這類應用程式必須支援搜尋通訊協定語法，並使用 [ [預設程式](default-programs.md) ] 功能註冊，以確保 Windows 的順暢體驗。

如果您開發的應用程式要在特定的桌面搜尋應用程式上使用或建立，您不應該依賴 **search：** protocol。 因為許多應用程式可能擁有 **搜尋：** 通訊協定，所以不保證您的目標桌面搜尋應用程式在任何指定的時間都有該應用程式。 相反地，您應該使用該目標桌面搜尋應用程式所定義的私人搜尋通訊協定。 這表示，要作為協力廠商應用程式平臺的桌面搜尋應用程式應該同時支援 **search：** protocol 和其專屬的搜尋通訊協定。

> [!Note]  
> **Search：** 通訊協定不會取代專屬的 [搜尋-ms：](../search/-search-3x-wds-qryidx-searchms.md) protocol。 應用程式仍然可以使用 **search-ms：** protocol 來啟動 Window search Explorer，或以無訊息方式查詢 Windows Search 索引子。

 

本主題包含下列項目：

-   [語法](#syntax)
-   [Windows Vista SP1 使用搜尋：通訊協定](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [範例](#examples)
-   [註冊處理通訊協定的應用程式](#registering-the-application-that-handles-the-protocol)
    -   [登錄專案](#registry-entries)
-   [相關主題](#related-topics)

## <a name="syntax"></a>Syntax

搜尋通訊協定會使用下列標準的 URL 編碼語法：


```C++
search:parameter=value[&parameter=value]&
```



語法一開始會識別通訊協定本身 (**搜尋：**) 。 參數/值組是傳遞給搜尋引擎的引數，如下表所述，其中顯示搜尋通訊協定語法的所有可能參數。



| 參數                                              | 值                                                         | 描述                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 查詢                                                  | URL 編碼的文字                                              | 使用者輸入的查詢文字。                                                                                                                                                                                                                                                            |
| [inputlocale](search-protocol-localeidentifiers.md)   | 任何有效的語言代碼識別碼 (LCID)                      | 識別查詢之輸入語言的 LCID。                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | 任何有效的 LCID                                                | 識別索引子之國際版本語言的 LCID。 預設值為 1033 (en-us) 。                                                                                                                                                                                |
| [粉](search-protocol-crumb.md)                     | AQS 語句                                                 | 此引數會限制要搜尋的範圍。 在 Windows Vista 中，搜尋通訊協定支援完整 AQS 以及引數的特殊實作為 `location` 。 在 Windows XP 中，除了與的特殊執行之外，搜尋通訊協定也支援完整 `kind` AQS `store` 。 |
| [語法](search-protocol-syntaxargument.md)           | NQS，AQS (不區分大小寫)                                  | 用來搜尋索引的查詢語法：自然查詢語法或 Advanced Query 語法 (AQS) 。 AQS 是預設值，而且一律會假設為已剖析且受支援。                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | 屬性系統中的任何有效屬性                   | 屬性，指定要用來堆疊結果的資料行。                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | 已儲存的搜尋檔案 (的完整指定路徑 \* 。搜尋-ms)  | 子查詢的結果會當做查詢的來源使用。 也就是說，會針對子查詢的結果搜尋查詢詞彙。                                                                                                                                               |
| displayname                                            | URL 編碼的字串                                            | 目前搜尋的名稱。                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Windows Vista SP1 使用搜尋：通訊協定

Windows Vista （含 SP1）有數個進入點，可從中呼叫 **search：** protocol。 這些進入點概述如下，以及與每個專案相關聯的一般語法。



| 搜尋通訊協定進入點 | Location         | 查詢呼叫                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **隨處搜尋**       | **開始** 功能表   | 搜尋： query =<*搜尋字詞*>                                   |
| **隨處搜尋**       | Windows 檔案總管 | 搜尋：查詢 =<*搜尋詞彙*>&連結 = 位置： <*位置*> |
| Windows 標誌鍵+F          | 任何位置         | 搜索：                                                              |
| CTRL+F                      | Windows 檔案總管 | 搜尋：查詢 =<*搜尋詞彙*>&連結 = 位置： <*位置*> |
| F3                          | **開始** 功能表   | 搜索：                                                              |
| F3                          | Windows 檔案總管 | 搜尋：查詢 =<*搜尋詞彙*>&連結 = 位置： <*位置*> |



 

Windows Vista SP1 搜尋通訊協定進入點不會利用搜尋通訊協定中的所有可能參數。 只有處理來自 Windows Vista SP1 呼叫的應用程式，才能使用下表作為其所需的最小值指南。



| 參數                                              | 由 Windows 使用？ | Windows Vista SP1 在呼叫搜尋時如何使用它：                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 查詢                                                  | Yes              | 使用者輸入的查詢文字。                                                                                                                                                                                                                                         |
| [粉](search-protocol-crumb.md)                     | Yes              | [連結](search-protocol-crumb.md) 會使用 `location` 引數來指定查詢的來源。                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Yes              | [子查詢](search-protocol-subquery.md)引數的結果會用來做為要搜尋之專案的範圍。 這通常會在使用者使用. 搜尋-ms 檔案來搜尋，然後從該搜尋內呼叫預設桌面搜尋應用程式時使用。 |
| [inputlocale](search-protocol-localeidentifiers.md)   | No               | 目前無法使用。                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | No               | 目前無法使用。                                                                                                                                                                                                                                                         |
| [語法](search-protocol-syntaxargument.md)           | No               | 目前無法使用。                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | No               | 目前無法使用。                                                                                                                                                                                                                                                         |
| displayname                                            | No               | 目前無法使用。                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>範例

如果使用者在 [開始] 功能表中輸入 **「Microsoft」** 並按一下 [ **隨處搜尋**]，則會進行結果搜尋通訊協定呼叫：


```C++
search:query=microsoft&
```



如果使用者在 C： MyFolder 內的 Windows 檔案總管中輸入「西雅圖」， \\ 然後按一下 [ **隨處搜尋**]，則會使用 '： ' 和 ' ' 的 escape 字元進行下列呼叫 \\ ：


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>註冊處理通訊協定的應用程式

由於有多個應用程式可以爭用搜尋通訊協定，因此您應該在安裝期間使用 [ [預設程式](default-programs.md) ] 功能來註冊您的應用程式，讓使用者能夠更輕鬆地設定預設值。 除了通常會在 Windows XP 下進行的安裝程式之外，Windows Vista 應用程式必須向 [預設程式] 功能註冊，讓應用程式和使用者可以順暢地設定預設值。

在使用者的電腦上安裝必要的二進位檔案之後，您的安裝常式應完成這些一般工作：

1.  將 Progid 寫入 **HKEY \_ 本機 \_ 電腦**，如下所述。 請注意，應用程式必須建立搜尋通訊協定的應用程式特定 Progid。
2.  索取電腦層級搜尋通訊協定關聯。
3.  使用 [預設程式](default-programs.md)來註冊應用程式，如 [註冊應用程式以搭配預設程式使用](default-programs.md)，以做為搜尋通訊協定的競爭者。

### <a name="registry-entries"></a>登錄項目

以下是虛構桌面搜尋應用程式（Contoso 搜尋）所需的登錄專案範例。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[進階查詢語法](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[預設程式](default-programs.md)
</dt> </dl>

 

 
