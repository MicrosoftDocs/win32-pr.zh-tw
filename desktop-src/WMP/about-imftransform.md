---
title: 關於 IMFTransform
description: 關於 IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
- Windows Media Player 外掛程式、IMFTransform 介面
- 外掛程式，IMFTransform 介面
- 數位信號處理外掛程式，IMFTransform 介面
- DSP 外掛程式，IMFTransform 介面
- IMFTransform 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b410702d63657261faa2fc8e7db123e05dcdc12c3096a49f8c0e2e36a41ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903578"
---
# <a name="about-imftransform"></a>關於 IMFTransform

**IMFTransform** 介面是必須由雙重模式的 DSP 外掛程式所執行的其中一個介面。 Windows Media Player 會呼叫 **IMFTransform** 介面的方法，以提供資料給外掛程式，並從外掛程式取回已處理的資料。 如需 **IMFTransform** 介面的完整檔，請參閱 Windows SDK 的媒體基礎一節。

**IMFTransform** 的方法可分類如下。

## <a name="methods-that-handle-format-negotiation"></a>處理格式協調的方法

Windows Media Player 會呼叫下列方法，以取得外掛程式所支援之資料格式的相關資訊。

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **SetInputType**
-   **SetOutputType**
-   **GetAttributes**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>指定或取得狀態資訊的方法

Windows Media Player 會呼叫下列方法來取得或設定與外掛程式目前狀態相關的值。

-   **SetInputType**
-   **SetOutputType**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType** 和 **SetOutputType** 用於格式化協商以及指定和取得狀態資訊。

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>處理緩衝處理和處理資料的方法

Windows Media Player 會呼叫下列方法，以起始外掛程式執行的各種處理常式，以執行數位信號處理。

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **In processevent.<**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**必要的介面**](required-interfaces.md)
</dt> </dl>

 

 




