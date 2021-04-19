---
description: 通訊會話的媒體是傳輸資料的形式。 媒體控制項可讓應用程式辨識各種不同的媒體類型，並調整媒體資料流程的各個層面，例如語音傳輸量。
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: 媒體控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dad56e3feef8493a70cf93152b225be2777848
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982142"
---
# <a name="media-control"></a>媒體控制項

通訊會話的媒體是傳輸資料的形式。 媒體控制項可讓應用程式辨識各種不同的媒體類型，並調整媒體資料流程的各個層面，例如語音傳輸量。

媒體控制項和資訊的可用性會隨著 TAPI 應用程式、服務提供者支援和本機通訊環境的類型而有很大的差異。 下列材質提供媒體控制項的一般描述。 TAPI 提供彈性的架構來執行控制項，因此最有趣的功能通常是指定的服務提供者。

在傳統電話語音下，一旦設定了通訊路徑，應用程式就幾乎不太能控制媒體串流。 TAPI 2 應用程式可存取某些功能，讓他們能夠在通話期間辨識和回應數位或音，並且可以使用 Wave API 在通訊會話期間對媒體執行額外的控制，否則就不會有媒體串流存取權。 如需這些函式的評論，請參閱《 TAPI 2.2 [媒體存取](./media-access.md) 總覽」或 TSPI [媒體存取](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) 總覽。

TAPI 3 引進 [媒體服務提供者](about-the-media-service-provider-msp-.md)，陡會增加與控制媒體或通訊會話的相關資訊。 TAPI 3 應用程式可以直接存取會話的媒體 [串流](stream-objects.md) 。 此會話中所涉及的每個媒體類型都會建立個別的資料流程，例如語音或影片。 某些 Msp 可能會執行子資料流程控制項，以進一步分割資料流程，例如參與者在 IPConf MSP 的情況下。



| TAPI 2.x 函數                                          | Description                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | 在指定的呼叫上起始已緩衝的數位收集。                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | 使用指定的信號模式，在指定的呼叫上起始指定之數位的產生，作為 inband 音。 |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | 產生指定之呼叫的指定 inband 語氣。                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | 啟用及停用未緩衝的偵測，以在呼叫上收到的數位。                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | 啟用及停用指定之呼叫的媒體類型偵測。                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | 啟用及停用電話上的 inband 音偵測。                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | 啟用及停用與指定的行、位址或呼叫相關聯之媒體資料流程上的控制項動作。             |



 



| TAPI 3.x 介面或方法                               | Description                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | 支援必須直接與裝置通訊的繼承應用程式。                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | 允許應用程式探索是否可以使用 Wave API 來控制舊版 TSP (預先 TAPI 3) 所建立的終端機。                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | 允許應用程式在資料流程上取得資訊;以啟動、暫停或停止資料流程;若要選取或取消選取資料流程上的終端機;以及取得資料流程上所選取的終端機清單。 |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | 允許應用程式列舉、建立或移除媒體資料流程。                                                                                                                                   |



 

 

 
