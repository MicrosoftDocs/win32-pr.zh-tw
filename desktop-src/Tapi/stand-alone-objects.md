---
description: TAPI 3 牽涉到許多與其五個主要 TAPI 物件無關的物件 (TAPI、Address、Call、CallHub 和 Terminal) 。
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Stand-Alone 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849233"
---
# <a name="stand-alone-objects"></a>Stand-Alone 物件

TAPI 3 牽涉到許多與其五個主要 TAPI 物件無關的物件 (TAPI、Address、Call、CallHub 和 Terminal) 。 [事件介面](./event-interfaces.md) 和 [列舉值介面](enumerator-interfaces.md) 是獨立的物件，而且會分開摘要。 以下摘要說明非事件和非列舉值的獨立介面。



| 介面                                             | 描述                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | 提供可讓自動化用戶端應用程式（例如 Visual Basic）取出集合資訊的方法。                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | 藉由提供修改集合的其他方法來擴充 [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) 。                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | 用來執行自動化的標準 COM 介面。                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | 用來取得物件介面指標的標準 COM 介面。                                                                                                                                             |
| [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | 允許應用程式在給定目前 [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) 指標的情況下，取得物件上另一個介面的分派指標。 適用于一些指令碼語言。 |
| [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | 提供可讓 TAPI 3 應用程式使用 [輔助電話語音](assisted-telephony-overview.md)的方法。                                                                                                |



 



| 介面                                  | 描述                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | 啟動、停止和暫停目前的動作，例如播放。                                                                                                             |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | 提供可讓應用程式執行這類作業的播放特定方法，例如，設定要播放及變更播放速度的檔案清單。              |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | 提供記錄特有的方法，可讓應用程式執行這類作業，例如設定記錄檔的名稱，以及變更錄製的持續時間。 |



 



| 介面                                                  | 描述                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | 從取出音訊格式，或設定播放軌的音訊格式。                                                                                             |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | 提供支援電話裝置所需之靜態音訊終端機物件的方法。 TAPI 3.1 Msp 必須在所有靜態音訊終端機上公開這個介面。 |



 

 

 
