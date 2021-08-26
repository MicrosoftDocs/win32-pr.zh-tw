---
description: DirectShow 中的 MPEG 2 支援
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: DirectShow 中的 MPEG 2 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9feaa24ea36b6f5e00e0f6ecd5db49ce37181f9d6d7348b3cfa27e64f7f2d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075798"
---
# <a name="mpeg-2-support-in-directshow"></a>DirectShow 中的 MPEG 2 支援

本節說明您可以在 DirectShow 中用來播放 MPEG 2 內容的元件。

> [!Note]  
> 雖然 DVD 影片是以 MPEG-2 為基礎，但本節並不說明 DVD 播放或導覽。 如需 DirectShow dvd 的詳細資訊，請參閱[dvd 應用程式](dvd-applications.md)。

 

MPEG-2 資料可以來自本機檔案，或來自即時來源（例如網路廣播或 D VHS 裝置）。 檔案播放稱為「 *提取模式* 」，因為剖析器篩選器會將檔案中的資料提取至篩選圖形。 即時來源稱為 *推送模式* ，因為來源篩選會將資料推送至圖形。

DirectShow 提供兩個可剖析 mpeg-2 系統資料流程的篩選：

-   [Mpeg-2 信號](mpeg-2-demultiplexer.md) ( "demux" ) ：此篩選器支援程式資料流程和傳輸資料流程的推送模式。 在 Windows XP 和更新版本中，它也支援程式資料流程的提取模式。
-   [Mpeg-2 分隔](mpeg-2-splitter.md)器：此篩選器支援舊版平臺上的程式資料流程提取模式。 此篩選在 Windows XP 及更新版本中已被取代。

若要使用 mpeg-2 demux 或 mpeg-2 分隔器，您必須有 DirectShow 相容的 mpeg-2 音訊和影片解碼器，以接受 packetized 的基本串流 (pe) 。

本節包含下列主題：

-   [MPEG 2 系統總覽](overview-of-mpeg-2-systems.md)
-   [使用 MPEG-2 信號信號](using-the-mpeg-2-demultiplexer.md)
-   [使用 MPEG-2 分隔器](using-the-mpeg-2-splitter.md)
-   [MPEG 範例屬性](mpeg-sample-properties.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PSI 剖析器篩選範例](psi-parser-filter-sample.md)
</dt> </dl>

 

 



