---
title: 摘要資訊屬性集
description: COM 會定義標準的通用屬性集，以儲存檔的摘要資訊。
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54f942d0c7f6c7d1ebc37feda80d55420ea6c8aaf896f4df15df2a5b7e7c0ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886824"
---
# <a name="the-summary-information-property-set"></a>摘要資訊屬性集

COM 會定義標準的通用屬性集，以儲存檔的摘要資訊。 摘要資訊屬性集必須儲存在資料流程物件中。 亦即，這個屬性集必須儲存為簡單的屬性集。 如需詳細資訊，請參閱[儲存體和資料流程物件的屬性集](storage-vs--stream-for-a-property-set.md)。

例如，若要建立 ANSI 簡單屬性集，您可以呼叫 [**IPropertySetStorage：： create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 來建立屬性集，指定 **PROPSETFLAG \_ ANSI** (simple 是屬性集) 的預設型別，然後使用 [**IPropertyStorage：： WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)的呼叫來寫入它。 若要讀取屬性集，您可以呼叫 [**IPropertyStorage：： ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)。

所有共用屬性集都是以 "005" 前置詞為 "" 的資料流程或儲存體名稱來識別 \\ (或 0x05) ，以顯示它是可在應用程式之間共用的屬性集。 摘要資訊屬性集不是例外狀況。 包含摘要資訊屬性集的資料流程名稱為： **" \\ 005SummaryInformation"**

透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面的 [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)或 [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)方法存取屬性時，不需要知道屬性集的資料流程名稱;在此情況下，只需要知道 (FMTID) 的格式識別碼。 摘要資訊屬性集的 FMTID 為： **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

此值的宣告可在標頭檔中作為 **FMTID \_ SummaryInformation**。 如需詳細資訊，請參閱 [預先定義的屬性集格式識別碼](predefined-property-set-format-identifiers.md)中的 FMTIDS。

下表列出摘要資訊屬性集的字串屬性名稱，以及各自的屬性識別碼和變數類型 (VT) 指標。 這些名稱通常不會儲存在屬性集中，而是從屬性識別碼值推斷而來。 此處所示的屬性識別碼字串專案對應至標頭檔中找到的定義。

| 名稱 | 屬性識別碼字串 | 屬性識別碼 | VT 類型 |
|------|--------------------|-------------|---------|
| Title | PIDSI \_ 標題 | 0x00000002 | VT \_ LPSTR  |
| 主旨 | PIDSI \_ 主旨 | 0x00000003 | VT \_ LPSTR |
| 作者 | PIDSI \_ 作者 | 0x00000004 | VT \_ LPSTR |
| 關鍵字 | PIDSI \_ 關鍵字 | 0x00000005 | VT \_ LPSTR |
| 註解 | PIDSI \_ 批註 | 0x00000006 | VT \_ LPSTR |
| 範本 | PIDSI \_ 範本 | 0x00000007 | VT \_ LPSTR |
| 上次儲存者 | PIDSI \_ LASTAUTHOR | 0x00000008 | VT \_ LPSTR |
| 修訂號碼 | PIDSI \_ REVNUMBER | 0x00000009 | VT \_ LPSTR |
| 總編輯時間 | PIDSI \_ EDITTIME | 0x0000000A | VT \_ FILETIME (UTC)  |
| 前次列印時間 | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC)  |
| 建立時間/日期 (請參閱下方的附注)  | PIDSI \_ 建立 \_ DTM | 0x0000000C | VT \_ FILETIME (UTC)  |
| 上次儲存的時間/日期 (請參閱下面的附注)  | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | VT \_ FILETIME (UTC)  |
| 頁面數目 | PIDSI \_ PAGECOUNT | 0x0000000E | VT \_ I4 |
| 單字數目 | PIDSI \_ WORDCOUNT | 0x0000000F | VT \_ I4 |
| 字元數 | PIDSI \_ >CHARCOUNT | 0x00000010 | VT \_ I4 |
| 縮圖 | PIDSI \_ 縮圖 | 0x00000011 | VT \_ CF |
| 建立應用程式的名稱 | PIDSI \_ APPNAME | 0x00000012 | VT \_ LPSTR |
| 安全性 | PIDSI \_ 安全性 | 0x00000013 | VT \_ I4 |

> [!NOTE]
> 針對 **建立時間/日期** 和 **上次儲存的時間/日期**，某些檔案傳輸方法（例如從 BBS 下載）不會正確地維護此資訊的檔案系統版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行摘要資訊屬性集](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




