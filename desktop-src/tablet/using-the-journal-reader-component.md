---
description: Microsoft Windows 筆記本 Note Reader 元件提供以程式設計方式讀取日誌格式的檔案。
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: 使用日誌讀取器元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943393"
---
# <a name="using-the-journal-reader-component"></a>使用日誌讀取器元件

Microsoft Windows 筆記本 Note Reader 元件提供以程式設計方式讀取日誌格式的檔案。

## <a name="component-overview"></a>元件總覽

日誌檔案的副檔名為 .jnt。 這個簡單的元件接受包含 .jnt 檔案的資料流程，並以 XML 格式傳回包含檔案內容的資料流程。 元件所傳回的 XML 會符合筆記本便箋讀取器架構。 此架構記載于 [日誌讀取器架構參考](journal-reader-schema-reference.md)中。

元件不提供寫出 .jnt 檔案的能力。

元件可用於非受控和受控版本。 未受管理的元件可在 journal.dll 動態連結程式庫 (DLL) 中取得。 受控版本位於 Microsoft.Ink.Journal.dll 元件 (，可轉散發至 Windows XP Tablet PC Edition 或 Windows Vista) ，或 Microsoft.Ink.dll。

> [!IMPORTANT]
>
> 從 Windows 10 開始，版本1607，journal.dll 不包含在 Windows 作業系統中。 該程式庫應視為已淘汰或已淘汰，且不應該使用。

 

### <a name="assembly-changes-of-note"></a>注意事項的元件變更

請務必留意元件的一些變更，其中包含與平板電腦開發人員套件1.7 版和 Windows Vista 作業系統隨附的版本之間所發行的「筆記本便箋讀取器」元件。

可以轉散發至 Windows XP 或 Windows Vista 的讀取器元件1.7 版本，包含在名為 Microsoft.Ink.Journal.dll 的元件中。 讀取器元件隨附于 Windows Vista 中，但已整合至核心 Microsoft.Ink.dll 元件。 這表示使用1.7 元件的應用程式必須將該元件重新發佈到其設定。

## <a name="using-the-component"></a>使用元件

筆記本便箋讀取器元件適合用來從日誌檔案中解壓縮筆墨資料和檔案的其他相關資訊。

### <a name="com"></a>COM

筆記本便箋讀取器 COM 元件位於檔案 Journal.dll 中，當您下載並執行筆記本便箋讀取器安裝檔案時，會安裝並註冊此元件。

COM 元件不支援 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面。

### <a name="managed"></a>受控

筆記本便箋讀取器管理的元件位於 Microsoft.Ink.JournalReader.dll 元件中。 當您執行筆記本便箋讀取器安裝檔案時，會在全域組件快取中安裝並註冊此元件。

加入元件的參考，以便在您的 managed 專案中使用它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IJournalReader 介面**](ijournalreader.md)
</dt> <dt>

[日誌讀取器架構參考](journal-reader-schema-reference.md)
</dt> </dl>

 

 
