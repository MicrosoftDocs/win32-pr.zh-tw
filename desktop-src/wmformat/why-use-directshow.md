---
title: 為何要使用 DirectShow
description: 為何要使用 DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows媒體格式 SDK，DirectShow
- Windows媒體格式 SDK，硬體
- 'Windows媒體格式 SDK、Windows Driver Model (WDM) '
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、硬體
- ASF (Advanced Systems Format) ，硬體
- 'Advanced Systems Format (ASF) 、Windows Driver Model (WDM) '
- 'ASF (Advanced Systems Format) 、Windows Driver Model (WDM) '
- DirectShow，關於
- DirectShow，硬體
- 'DirectShow，Windows Driver Model (WDM) '
- Windows (WDM) 的驅動程式模型
- 'WDM (Windows Driver Model) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5edce48be7a806011ba59ab5a2c5328840a18399f6f7eea65d649d52c62402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839418"
---
# <a name="why-use-directshow"></a>為何要使用 DirectShow？

應用程式可能會直接使用 DirectShow 而不是 Windows 媒體格式 SDK 的主要原因有兩個：為了方便使用 DirectShow 串流架構，以及存取硬體。

## <a name="convenience"></a>便利

使用 DirectShow 串流架構，只需要幾個方法呼叫來播放 Windows Media 音訊或 Windows Media 視訊的檔案。 也簡化了建立檔案的程式。 您只需使用篩選上的 **IConfigAsfWriter** 介面來指定設定檔，DirectShow 會自動載入轉譯或寫入資料流程所需的元件，並提供傳輸和同步處理媒體資料流程程的機制。 將不同格式的內容轉換成 Windows 媒體格式時，DirectShow 特別有用。 您可以建立 DirectShow 篩選圖形來解碼各種不同的檔案和壓縮類型，然後將已解碼的資料流程饋送到[WM ASF 寫入](wm-asf-writer-filter.md)器篩選器中。 相較之下，此 SDK 中的 UncompAVItoWMV 範例只適用于未壓縮的 AVI 檔案。 文字資料流程和任意資料流程也可以透過 DirectShow 建立及/或轉譯，但這可能需要您建立自訂的 DirectShow 篩選器來處理這些資料流程。

## <a name="access-to-hardware"></a>存取硬體

DirectShow 是應用程式程式碼存取 Windows Driver Model (WDM) 型硬體裝置（例如 1394 DV 攝影機、電視調諧器和 USB 網路攝影機）的唯一方法。 如果您的應用程式必須直接從以 WDM 為基礎的硬體裝置來捕捉資料，並轉碼為 Windows 媒體格式，且 Windows 媒體編碼器 SDK 不符合您的需求，則 DirectShow 是唯一的替代方案。 DirectShow 也可以用來根據 Windows 的影片來存取舊版裝置。

 

 




