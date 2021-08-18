---
description: 本章節描述 Microsoft 媒體基礎的一般設計。 如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱媒體基礎程式設計指南。
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: 媒體基礎架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcc95b1fdb39ad7d0e90e44b66df0dd7eb3c06418c16b4efc452abba4a9738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974211"
---
# <a name="media-foundation-architecture"></a>媒體基礎架構

本章節描述 Microsoft 媒體基礎的一般設計。 如需使用媒體基礎進行特定程式設計工作的詳細資訊，請參閱 [媒體基礎程式設計指南](media-foundation-programming-guide.md)。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                         | 描述                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [媒體基礎架構的總覽](overview-of-the-media-foundation-architecture.md)<br/> | 提供媒體基礎架構的高層級總覽。<br/>                                                                                                                                                                                                               |
| [媒體基礎基本](media-foundation-primitives.md)<br/>                                     | 描述在媒體基礎中使用的一些基本介面。<br/> 幾乎所有的媒體基礎應用程式都會使用這些介面。<br/>                                                                                                                       |
| [媒體基礎平臺 Api](media-foundation-platform-apis.md)<br/>                               | 描述核心媒體基礎函式，例如非同步回呼和工作佇列。<br/> 某些應用程式可能會使用平台層級的介面。 此外，自訂外掛程式（例如媒體來源和 MFTs）會使用這些介面。<br/>                                       |
| [媒體基礎管線](media-foundation-pipeline.md)<br/>                                         | 媒體基礎管線層是由媒體來源、MFTs 和媒體接收器所組成。 大部分的應用程式不會直接在管線層呼叫方法。 相反地，應用程式會使用其中一個較高的層級，例如媒體會話或來源讀取器和接收寫入器。<br/> |
| [媒體會話](media-session.md)<br/>                                                                 | 媒體會話會管理媒體基礎管線中的資料流程。<br/>                                                                                                                                                                                                           |
| [來源讀取程式](source-reader.md)<br/>                                                                 | 來源讀取器可讓應用程式從媒體來源取得資料，而不需要直接呼叫媒體來源 Api 的 applicating。 來源讀取器也可以執行壓縮資料流程的解碼。<br/>                                                            |
| [受保護的媒體路徑](protected-media-path.md)<br/>                                                   | 受保護的媒體路徑 (PMP) 提供受保護的環境來播放 premium 影片內容。 撰寫媒體基礎的應用程式時，不需要使用 PMP。 <br/>                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體基礎](about-the-media-foundation-sdk.md)
</dt> <dt>

[媒體基礎：基本概念](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[媒體基礎和 COM](media-foundation-and-com.md)
</dt> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </dl>

 

 




