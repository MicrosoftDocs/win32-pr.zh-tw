---
description: 您的全球化應用程式必須定義各種使用者介面元素，例如功能表、對話方塊、說明字串，以及其他以當地語系化資源表示的專案。
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: MUI 資源管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000257"
---
# <a name="mui-resource-management"></a>MUI 資源管理

您的全球化應用程式必須定義各種使用者介面元素，例如功能表、對話方塊、說明字串，以及其他以當地語系化資源表示的專案。 使用者介面語言會成為應用程式的其中一個設定。 本節說明 MUI 資源技術，我們建議您使用這些資源技術來建立您的應用程式資源。

## <a name="features-of-the-mui-resource-technology"></a>MUI 資源技術的功能

在 Windows Vista 和更新版本中公開的 MUI 資源技術具有下列特性：

-   特定語言的資源檔會與應用程式程式碼二進位檔分開儲存，因此程式碼變更不會影響資源。
-   多個語言的資源可以部署在單一安裝中，或針對每個語言個別安裝。
-   資源會根據使用者設定的應用程式語言來載入和顯示。

這項技術會將語言特定檔案中定義的資源與特定版本的語言中性 (LN) 檔產生關聯。 LN 檔案是 Win32 PE 檔案，代表應用程式程式碼二進位檔和非語言相關的資源。 檔案的關聯會使用反映在所有相關聯檔案所含之資源設定資料中的總和檢查碼。 資源載入器會使用總和檢查碼來確認檔案保存相同版本的必要資源。 它也會以其資料夾名稱驗證語言特定檔案中的語言。 如果未建立適當的關聯，則載入器不會載入資源檔。

具體而言，主要總和檢查碼的計算是從檔案的主要和次要版本號碼，以及檔案名 (區分大小寫的) ，這些都是從版本資源取得的。 此總和檢查碼不應該在相同元件的 RTM 和 service pack 版本之間變更。 此外，也會使用服務總和檢查碼來決定要載入之特定語言資源檔的適當版本。 此總和檢查碼是根據檔案中可當地語系化的資源來計算。

MUI 提供兩個資源公用程式，可供您用來準備應用程式的資源檔。 MUI 專屬公用程式（稱為 MUIRCT）可讓您建立 LN 檔和相關聯的語言特定資源檔。 在 Windows Vista 和更新版本上，Windows RC 編譯器也已經過修改，可根據 MUI 資源技術來建立這些檔案。 如需這些工具的語法和詳細資料，請參閱 [資源公用程式](resource-utilities.md)。

## <a name="ln-file"></a>LN 檔

MUI 應用程式的 LN 檔案包含可執行程式碼和語言中立的資源，這些資源是由應用程式的所有語言版本所共用和安裝。

## <a name="language-specific-resource-file"></a>Language-Specific 資源檔

特定語言的資源檔通常會包含使用者介面字串，以及需要針對特定語言進行當地語系化的其他元素。 您的 MUI 應用程式會針對每個支援的語言使用一個特定語言的資源檔。 適用于每個語言專屬資源檔的應用程式的 LN 檔案都相同。

使用 MUI 資源技術建立時，語言特定檔案的副檔名為 "mui"，並以下列方式處理：

-   與指定之 LN 檔案相關聯的特定語言檔案全都共用相同的檔案名，這是藉由將副檔名 ". mui" 新增至完整檔案名 (加上對應之 LN 檔案的副檔名) 來形成相同的名稱。 例如，名為 "Myfile.dll" 的 LN 檔案包含名為 "Myfile.dll mui" 的語言特定檔案。
-   特定語言的檔案位於包含 LN 檔案之資料夾的子資料夾中。 每個資料夾名稱都會反映出語言。

## <a name="resource-configuration-data"></a>資源設定資料

為了建立 LN 檔案與其語言特定檔案的關聯，MUI 資源技術會使用資源設定資料，包括總和檢查碼。 資源建立程式會將這項資訊放在每個 LN 和語言特定檔案的 RC Config 區段中。 您可以透過 MUIRCT 公用程式取得這項資訊的人們可讀取形式。 如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於多語系消費者介面](about-multilingual-user-interface.md)
</dt> <dt>

[資源公用程式](resource-utilities.md)
</dt> </dl>

 

 



