---
description: 筆墨分析程式庫有四個層級： Windows Forms、WPF、COM 和基底層。 本節說明使用每個圖層的時機。
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: 筆墨分析 API 使用方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943259"
---
# <a name="ink-analysis-api-usage"></a>筆墨分析 API 使用方式

筆墨分析程式庫有四個層級： Windows Forms、WPF、COM 和基底層。 本節說明使用每個圖層的時機。

## <a name="ink-analysis-api-overview"></a>筆墨分析 API 總覽

筆墨分析程式庫是設計用來在各種支援的程式設計環境中使用。 有四個基本層可讓您的應用程式使用筆墨分析。 這些層級如下：

-   Windows Forms 層
-   WPF 層
-   COM 層
-   基底層

### <a name="windows-forms-applications"></a>Windows Forms 應用程式

您可以藉由新增下列程式庫的參考，在您的 managed 專案中使用筆墨分析 API：

-    (Microsoft.Ink.Analysis.dll) 的 Microsoft Ink 分析
-   筆墨檔分析庫 (IACore.dll) 

在 Windows Forms 應用程式中，您很有可能會使用程式庫搭配在 Microsoft Tablet PC API 1.7 版元件中找到的標準 Tablet PC 平臺物件。 確定您也有下列參考：

-   Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll) 

### <a name="windows-presentation-framework-applications"></a>Windows Presentation Framework 應用程式

您可以在 WPF 專案中使用筆墨分析 API，方法是將參考新增至 IAWinFX.dll 元件中的 System.object 命名空間中定義的筆墨分析成員。 SDK 會安裝此元件。

### <a name="com-applications"></a>COM 應用程式

非自動化 COM 應用程式應該使用筆墨分析 Api 的 COM 層。

輸入特定的 [CoNtextNode](/previous-versions/ms551996(v=vs.100)) 物件（例如 [ParagraphNode](/previous-versions/ms580136(v=vs.100))、 [InkWordNode](/previous-versions/ms580133(v=vs.100))和其他物件）不會用於 COM 層。 相反地，您應該在標準 [**ICoNtextNode**](icontextnode.md)介面上使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) 。

您必須 \# 包含 "IACom .h"。 您很可能會使用程式庫搭配使用 Tablet PC 平臺筆墨物件，因此您也應該 \# 包含 "msinkaut"。

### <a name="rts-and-other-applications"></a>RTS 和其他應用程式

筆墨分析基底圖層的運作方式不同于其他專案，它會使用點資料進行分析，而不是 [筆劃](/previous-versions/ms552692(v=vs.100)) 物件。 您可以直接使用基底層而不是使用 Windows forms 或 COM 層的範例，包括不使用第一代 Tablet PC 平臺筆墨物件的應用程式，或是使用 [**RealTimeStylus**](realtimestylus-class.md) api 來管理手寫筆輸入的應用程式，而不是使用 Tablet Pc 平臺 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件。

## <a name="32-bit-support-only"></a>僅限32位支援

請注意，只有在32位的進程中才支援筆墨分析程式庫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[筆墨分析總覽](ink-analysis-overview.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 
