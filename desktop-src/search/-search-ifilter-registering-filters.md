---
description: 您必須註冊篩選處理常式。 您也可以透過登錄或使用 ILoadFilter 介面，找出給定副檔名的現有篩選處理常式。
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: 註冊篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112449"
---
# <a name="registering-filter-handlers"></a>註冊篩選處理常式

您必須註冊篩選處理常式。 您也可以透過登錄或使用 [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) 介面，找出給定副檔名的現有篩選處理常式。

本主題的組織方式如下：

- [註冊 Windows Search 的篩選處理常式](#registering-filter-handlers)
  - [註冊篩選處理常式的過時方法](#obsolete-approach-for-registering-filters-handlers)
- [取代現有的篩選處理常式](#replacing-existing-filter-handlers)
- [尋找指定副檔名的篩選處理常式](#finding-a-filter-handler-for-a-given-file-extension)
- [其他資源](#additional-resources)
- [相關主題](#related-topics)

> [!NOTE]  
> 篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的實作為。

## <a name="registering-filters-handlers-for-windows-search"></a>註冊 Windows Search 的篩選處理常式

下表列出您註冊新的通訊協定處理常式或尋找現有的通訊協定處理常式所需的 Guid。

| GUID                                     | 已定義使用者或應用程式 | Description                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89BCB740-6119-101A-BCB7-00DD010655AF** | 應用程式                 | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面 GUID 是所有篩選處理常式的登錄機碼常數。 |
| **{PersistentHandlerGUID}**              | User                        | 這是持續性處理常式的 GUID。                                                              |
| **{FilterHandlerCLSID}**                 | User                        | 這是篩選處理常式 (CLSID) 的類別識別碼。                                              |
| **{ApplicationGUID}**                    | User                        | 這是中繼 (匯總) GUID。                                                                |

篩選處理常式必須在 HKEY \_ 本機電腦上註冊 \_ ，因為 SearchFilterHost.exe 正在系統帳戶下執行，因此無法存取 \_ 登入使用者的 HKEY 目前使用者的登錄機碼 \_ 。 此外，Users 群組必須擁有篩選處理常式 .dll 本身的讀取和執行存取權，因為 SearchFilterHost.exe 會移除所有的系統管理員許可權，而且只允許非系統管理員許可權。 因為預設 Visual Studio 專案位置是在目前使用者的目錄中，所以不會將讀取權限授與 Users 群組，所以您必須移動 .dll 或變更 Acl 以允許 SearchFilterHost.exe 存取。

當您註冊新的篩選處理常式時，建議您使用描述性名稱，例如 HTML IFilter。

**若要註冊新的篩選器處理常式：**

1. 指定將使用篩選處理常式的延伸模組和持續性處理常式 GUID：

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. 使用下列索引鍵和值註冊您的篩選器處理常式：

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a>註冊篩選處理常式的過時方法

不建議使用此方法。 您可以針對表示元件物件模型 (COM) 類別和/或副檔名的 CLSID 註冊篩選。 如果您需要註冊類別的篩選處理常式，以及類別內的副檔名不同的篩選處理常式，您可以註冊這兩個篩選準則。 請注意，針對副檔名所註冊的篩選處理常式會優先于 CLSID 的篩選處理常式。

這些專案是標準的 OLE 登錄專案，最多可包含類別 **CLSID \\ {ApplicationGUID}** 的專案。 DLL sample.dll 會針對 .txt 類別來執行物件行為。 請注意額外的專案 PersistentHandler。 這個專案會指定負責代理範例類別之持續性物件要求的類別。 **PersistentAddinsRegistered** 下的專案會識別為名為 **89BCB740-6119-101A-BCB7-00DD010655AF** (IID IFilter) 的介面負責的執行 \_ 。 執行 **IID \_ IFilter** 的類別具有標準的 OLE 登錄專案。 InprocServer32 DLL 是透過標準的 OLE 機制載入的。

Windows Search 觀察為篩選處理常式指定的執行緒模型。 當執行緒模型設定為 [ **兩者**] 時，篩選處理常式必須為安全線程;否則，如果它不是安全線程，請指定 **公寓**。 請注意，篩選處理常式應該一律為安全線程。

下列範例登錄專案適用于註冊類別和副檔名的篩選處理常式。 **{PersistentHandlerGUID}** 和 **{FilterHandlerCLSID}** 是用來做為變數，指出必須由篩選處理常式的建立者指定的值。 值的類型是 REG \_ SZ。

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a>取代現有的篩選處理常式

我們建議您不要將內建的篩選器處理常式取代為一般檔案類型，例如 .txt、.doc、.html、. url 等等，因為這樣做可能會對其他系統元件造成不良的影響。 編制電子郵件訊息內文的索引取決於 .txt、.html 和 .rtf 篩選器處理常式，例如。

如果將檔案類型的新篩選處理常式安裝為現有篩選註冊的取代，則安裝程式應儲存目前的註冊，並在新的篩選器處理常式卸載時還原。 沒有任何機制可連結篩選。 因此，新的篩選處理常式會負責複寫舊篩選器的任何必要功能。

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>尋找指定副檔名的篩選處理常式

您可以使用 [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) 介面來尋找給定副檔名的篩選處理常式。 下列範例登錄專案說明如何針對 HTML 檔案進行這項操作。 在此範例中，會 nlhtml.dll HTML 檔案的篩選處理常式。 值的類型是 REG \_ SZ。

**若要尋找指定副檔名的篩選處理常式：**

1. 檢查已篩選之檔案類型的副檔名是否有在登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別下註冊的持續性處理常式。 如果是，請將此機碼視為 {PersistentHandlerGUID}。

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. 如果沒有針對延伸模組註冊的持續性處理常式，請在登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別下尋找與檔案類型相關聯的 CLSID。 讓此機碼為 {ApplicationGUID}。 然後判斷是否已為 CLSID 註冊持續性處理常式：使用 {ApplicationGUID} 找出 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ clsid \\ {ApplicationGUID} 專案的持續性處理常式。 讓此機碼為 {PersistentHandlerGUID}。

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. 判斷持續性處理常式的 GUID：使用 {PersistentHandlerGUID} 尋找檔案類型的持續性處理常式 GUID。 登錄專案 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ {PersistentHandlerGUID} PersistentAddinsRegistered 89BCB740-6119-101A-BCB7-00DD010655AF 下的值會 \\ \\ 產生此檔案類型的持續性處理常式 GUID。 讓此機碼為 {FilterHandlerCLSID}。

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. 判斷篩選處理常式：使用上一個步驟中所決定的 {FilterHandlerCLSID} 在 [ \\ \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32] 專案底下找到篩選處理常式。 在此範例中，使用的描述性篩選處理常式名稱是 HTML IFilter。

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a>其他資源

- [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 **ifilter** 介面的 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)基礎類別。
- 如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
- 如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
- 若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。

## <a name="related-topics"></a>相關主題

[開發篩選處理常式](-search-ifilter-conceptual.md)

[關於 Windows Search 中的篩選處理常式](-search-ifilter-about.md)

[在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)

[從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)

[Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)

[在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)

[測試篩選處理常式](-search-ifilter-testing-filters.md)
