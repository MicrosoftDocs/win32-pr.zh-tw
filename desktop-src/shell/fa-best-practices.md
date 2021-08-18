---
description: 下列清單是您在使用檔案關聯時應該使用的建議最佳作法。
title: 檔案關聯的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8cfa57faea9423af31e494c37d97af2b61d690095fb669a6a9b47109f6e97e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094213"
---
# <a name="best-practices-for-file-associations"></a>檔案關聯的最佳作法

下列清單是您在使用檔案關聯時應該使用的建議最佳作法。

-   [不要從登錄複製檔案關聯](#do-not-copy-file-associations-from-the-registry)
-   [盡可能避免 Hard-Coding 的路徑](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [一律以引號括住展開字串](#always-wrap-expanding-strings-in-quotation-marks)
-   [請勿將自動播放/自動播放與檔案關聯混淆](#do-not-confuse-autoplayautorun-with-file-associations)
-   [請勿混淆 Internet Explorer MIME 資料庫與檔案關聯](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [使用正確格式和建立版本的 Progid](#use-properly-formed-and-versioned-progids)
-   [請勿使用簡短的副檔名](#do-not-use-short-file-name-extensions)
-   [在 IANA MIME 資料庫中註冊新的檔案類型](#register-new-file-types-in-the-iana-mime-database)
-   [使用 Windows Web 服務註冊檔案關聯](#sign-up-with-the-windows-web-service-for-file-associations)
-   [相關主題](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a>不要從登錄複製檔案關聯

建議您不要從登錄複製現有的檔案關聯。 這通常會導致傳播格式不正確的檔案關聯。 相反地，您應該遵循檔案 [關聯範例案例](fa-sample-scenarios.md)中所述的步驟。

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a>盡可能避免 Hard-Coding 的路徑

如同程式碼的程式碼路徑可能會造成問題，登錄的硬式編碼路徑也會導致問題。 相反地，您應該使用登錄展開字串 (REG \_ EXPAND \_ SZ) 在適用的情況下提供獨立路徑。 例如，不要使用這個方法：

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

您應使用此方法：

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a>一律以引號括住展開字串

展開字串時可以包含空格。 由於空格通常會被視為引數分隔符號，因此在某些情況下會造成問題。 例如，用來叫用 Myprogram.exe 的命令可以儲存在登錄中，如下所示：

`%SYSTEMROOT%\MyProgram %1 %2`

Myprogram.exe 預期 %1 是檔案名的完整路徑，而 %2 是表示某些動作的參數。 如果使用引數 **c： \\ Program Files 執行此命令 \\ 我的檔 \\document.txt** 和 **/print**，並假設有 C： WINNT 的 SYSTEMROOT \\ ，它會展開為：

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

在此情況下，Myprogram.exe 會將第一個引數解釋為 C： \\ Program，而第二個引數是檔案 \\ My，這不是預期的行為。 如果展開的字串是以引號括住，就會正確地解讀引數，如下所示：

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a>請勿將自動播放/自動播放與檔案關聯混淆

檔案關聯在某些方面與自動播放/自動播放類似。 不過，自動播放/自動播放會提供與檔案關聯所提供不同的不同設備。 如需詳細資訊，請參閱 [建立啟用自動安裝的 Cd-rom 應用程式](autoplay.md)。

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a>請勿混淆 Internet Explorer MIME 資料庫與檔案關聯

檔案關聯類似于 Windows 的 Internet Explorer MIME 資料庫，在該檔案類型中可以 (，而且應該) 包含 MIME 類型定義。 不過，Internet Explorer MIME 資料庫是分開的，與檔案關聯不同。

## <a name="use-properly-formed-and-versioned-progids"></a>使用正確格式和建立版本的 Progid

一律使用已建立版本的 [progid](fa-progids.md)，即使只有一個版本的 ProgID。 已建立版本的 Progid 有助於避免 ProgID 衝突和覆寫。 它們也可讓不同版本的應用程式並存。

## <a name="do-not-use-short-file-name-extensions"></a>請勿使用簡短的副檔名

完整的副檔名提供下列優點：

-   簡短延伸的有限長度使其容易發生 *延伸衝突。* 使用相同的延伸模組來分類多個檔案類型時，會發生延伸衝突。 使用 long 擴充功能可大幅降低衝突的機率。
-   簡短檔案名通常有點難懂。 長延伸模組較有意義，因為其他資訊可以內嵌在延伸模組中。

如需詳細資訊，請參閱 [檔案名延伸](fa-file-extensions.md)。

## <a name="register-new-file-types-in-the-iana-mime-database"></a>在 IANA MIME 資料庫中註冊新的檔案類型

 (IANA 的網際網路指派號碼授權單位) 保留已註冊 MIME 類型的公用資料庫。 在定義新的公用檔案類型時，建議您也為檔案類型定義 MIME 類型，並向 IANA 註冊此類型。 註冊不會產生任何費用。

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a>使用 Windows Web 服務註冊檔案關聯

應用程式開發人員可以註冊 Windows Web 服務，讓使用者用來尋找可在特定檔案類型上操作的應用程式。 使用 web 服務註冊的程式會在[Windows 檔案關聯系統的內建程式](https://support.microsoft.com/kb/929149)中詳細說明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案關聯範例案例](fa-sample-scenarios.md)
</dt> <dt>

[在 Windows Vista 和更新版本中管理預設應用程式的指導方針](vista-managing-defaults.md)
</dt> <dt>

[預設程式](default-programs.md)
</dt> <dt>

[ (SPAD) 設定程式存取和電腦預設值 ](cpl-setprogramaccess.md)
</dt> </dl>

 

 



