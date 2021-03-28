---
description: 本主題說明如何建立新的檔案類型，以及如何將應用程式與您的檔案類型和其他妥善定義的檔案類型產生關聯。
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: 檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973244"
---
# <a name="file-types"></a>檔案類型

本主題說明如何建立新的檔案類型，以及如何將應用程式與您的檔案類型和其他妥善定義的檔案類型產生關聯。 共用通用副檔名的檔案 ( .doc、.html 等) 屬於相同的 *類型*。 例如，如果您建立新的文字編輯器，則可以使用現有的 .txt 檔案類型。 在其他情況下，您可能需要建立新的檔案類型。

本主題的組織方式如下：

-   [公用和私用檔案類型](#public-and-private-file-types)
-   [註冊檔案類型](#registering-a-file-type)
    -   [設定選擇性的子機碼和檔案類型延伸模組屬性](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [卸載期間刪除登錄資訊](#deleting-registry-information-during-uninstallation)
-   [支援開放中繼資料的檔案類型](#file-types-that-support-open-metadata)
-   [相關主題](#related-topics)

您可以在下列主題中找到其他資訊：

-   [如何選擇檔案類型延伸模組](how-to-choose-a-file-type-extension.md)
-   [如何定義檔案類型屬性](./how-to-define-file-type-attributes.md)
-   [如何在 [開啟檔案] 對話方塊中加入應用程式](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [如何從非關聯檔案類型的開啟檔案對話方塊中排除應用程式](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>公用和私用檔案類型

公用檔案類型也稱為熱門或之間爭論類型，因為競爭應用程式可能會想要與這些檔案類型相關聯。 公用檔案類型的特性包括：

-   它們通常是由標準主體所定義，而且/或由其定義組織作為交換格式來升級。
-   它們通常會在電腦和使用者之間進行不同用途的交換。
-   它們必須在許多不同的平臺上受到支援。
-   來自多個廠商的應用程式很可能會處理它們。

以下是一些被視為公用的檔案類型範例：圖像檔案類型 .png、.gif、.jpg 和 .bmp，以及音訊類型 .wav、mp3 和 au。

與公用檔案類型不同的是，私用或專屬檔案類型的格式通常只有一個應用程式或廠商可執行和瞭解。 因此，私用檔案類型通常不容易發生應用程式之間的衝突。 某些檔案類型可以啟動為私用檔案類型，但之後會變成公用檔案類型。

> [!Note]  
> Windows 不會區分公用和私用檔案類型。 差別僅與決定您選擇的檔案類型註冊有關。

 

## <a name="registering-a-file-type"></a>註冊檔案類型

若要將檔案類型與現有的應用程式產生關聯，請在登錄中找出應用程式 ProgID。 若要將檔案類型與新的應用程式產生關聯，請定義應用程式的 ProgID。 如需定義新 ProgID 的詳細資訊，請參閱程式 [設計識別碼](fa-progids.md)。

檔案名延伸子機碼具有下列一般格式：*延伸* = *ProgID*。 副檔名子機碼會儲存在 **HKEY \_ 類別 \_ 根** 子樹中。

在登錄中建立檔案類型的子機碼時，請務必包含前置期間 ( ) 。 例如，如果您想要使用名為 Myprogram.exe 的應用程式開啟副檔名為 myp 的檔案類型和長副檔名. myp 檔案，請使用下列語法：

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

如上一個範例所示，如果您也 ( 登錄簡短的副檔名) ，您也應該為完整的延伸模組建立子機碼 (. myp-file) 。 如需詳細資訊，請參閱 [檔案類型處理常式](fa-file-extensions.md)。

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>設定選擇性的子機碼和檔案類型延伸模組屬性

登錄中的檔案類型延伸模組專案有數個選擇性的子機碼和屬性。

下表說明檔案關聯所使用的檔案類型延伸模組專案。 所有值都是 **REG \_ SZ** 型別。



| 登錄項目  | 動作                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 預設         | 將擴充子機碼的預設值設定為其所連結的 ProgID。                                                                                                                                                                                                                                                 |
| 內容類型    | 將內容類型值設定為檔案類型的 MIME 內容類型。                                                                                                                                                                                                                                                                   |
| OpenWithList    | 請勿使用。 這個子機碼包含應用程式的一或多個應用程式子機碼，而這些應用程式會出現在檔案類型的 [ **開啟檔案** ] 對話方塊專案中，而且只適用于 Windows XP 之前作業系統上的 .exe 應用程式。 請改用 OpenWithProgIds。                                                            |
| OpenWithProgIds | 此子機碼包含這個檔案類型的替代 Progid 清單。 這些 Progid 的程式會顯示在 [ **開啟檔案** ] 功能表中，並可作為檔案類型的預設 Windows Store 應用程式。 每當應用程式藉由變更預設值來接管此檔案類型時，也應該在此清單中新增一個專案。 |
| PerceivedType   | 將 PerceivedType 值設定為檔案所屬的 PerceivedType （如果有的話）。 Windows Vista 之前的 Windows 版本不會使用這個字串。 如需詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。                                                                           |



 

副檔名的一般格式如下所示。 所有專案類型都是 **REG \_ SZ** 型別。

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

有關檔案類型的重要考慮包括：

-   **HKEY \_ 類別 \_ 根** 子樹是藉由合併 HKEY 的 **\_ 目前 \_ 使用者** \\ **軟體** \\ **類別** 和 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** 所形成的視圖
-   一般情況下， **HKEY \_ 類別 \_ 根目錄** 的目的是要讀取，但不是寫入。 如需詳細資訊，請參閱 [HKEY \_ 類別的 \_ 根](../sysinfo/hkey-classes-root-key.md) 文章。
-   若要在特定電腦上全域註冊檔案類型，請在 [ **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別**] 子機碼中建立檔案類型的專案。
-   若要讓目前的使用者可以看到檔案類型註冊，請在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼中建立檔案類型的專案。
-   應用程式可以提供自己的動詞命令，例如開啟或播放，如下列登錄範例所示。

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    動詞子機碼的子機碼包含命令列和 drop target 方法： **command** 和 **DropTarget**。

-   當您建立或變更檔案關聯時，請務必通知系統您已進行變更。 若要這麼做，請呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 並指定 **SHCNE \_ ASSOCCHANGED** 事件。 如果您未呼叫 **SHChangeNotify**，則在重新開機系統之前，可能無法辨識變更。
-   若要取得有關檔案關聯的登錄資訊，請使用 [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 介面。 如需示範此程式的案例，請參閱檔案 [關聯範例案例](fa-sample-scenarios.md)。

> [!Note]  
> 應用程式 **路徑** 和 **應用程式** 登錄子機碼都是用來代表應用程式註冊和控制系統的行為。 如需此功能的詳細資訊，請參閱 [應用程式註冊](app-registration.md)。

 

### <a name="deleting-registry-information-during-uninstallation"></a>卸載期間刪除登錄資訊

卸載應用程式時，與該應用程式相關聯的 Progid 和其他大部分的登錄資訊都應該在卸載過程中刪除。 不過，已取得檔 (類型擁有權的應用程式，會將檔案類型的 **HKEY \_ 類別 \_ 根目錄** 的預設值設定 \\ 為應用程式) 的 ProgID，所以不應該嘗試在卸載時移除該值。 將資料保留為預設值，可避免判斷其他應用程式是否已取得檔案類型的擁有權，並在安裝原始應用程式之後覆寫預設值的困難。 只有當 ProgID 找到已註冊的 ProgID 時，Windows 才會遵循預設值。 如果 ProgID 已取消註冊，則會予以忽略。

請注意，其他的檔案類型擁有權資訊會儲存在 [ **HKEY \_ 目前 \_ 使用者**] 子樹中，而且只有在註冊它所參考的應用程式時才會使用。 因此，在卸載應用程式時，不需要移除這種資料。

例如，以下顯示在卸載應用程式之前的登錄狀態：

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

以下顯示在卸載應用程式之後，這些登錄專案的狀態。

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>支援開放中繼資料的檔案類型

在 Windows 7 和更新版本中，下列檔案類型支援開放中繼資料。



| 檔案類型                                                               | 副檔名                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Office 2007 檔                                                   | .docx、.xlsx、.pptx                                           |
| Office 97-2003 檔                                                | .doc、.xls、.ppt                                              |
| 已儲存的搜尋                                                            | 。搜尋-ms                                                    |
| Windows Media 格式 (Advanced 串流格式 (ASF) 容器)  | .wmv、.wma                                                    |
|  (的屬性處理常式)                                                   | m4a、. m4v、. mp4v、m4p、m4b、3gp、3gpp、.3gp2、mov |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[程式設計識別碼](fa-progids.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

 

 
