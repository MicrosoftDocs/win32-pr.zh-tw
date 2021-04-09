---
description: RealTimeStylus 物件原本就不會收集筆跡。 若要使用 RealTimeStylus 收集筆跡，請建立筆墨收集器外掛程式。
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847781"
---
# <a name="ink-collection-plug-ins"></a>Ink-Collection 外掛程式

[**RealTimeStylus**](realtimestylus-class.md)物件原本就不會收集筆跡。 若要使用 **RealTimeStylus** 收集筆跡，請建立筆墨收集器外掛程式。

以下是在收集筆墨的表單上使用 [**RealTimeStylus**](realtimestylus-class.md) 物件的最基本案例。

1.  建立可執行 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的表單。
2.  建立 [**RealTimeStylus**](realtimestylus-class.md) 物件，並將它附加至表單上的控制項。
3.  在表單的 [DataInterest](/previous-versions/ms574886(v=vs.100)) 屬性中，設定 StylusDown、封包和 StylusUp 通知的興趣。
4.  在表單的 [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)、封 [**包**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)和 [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) 方法中，新增程式碼以處理從表單之 [**RealTimeStylus**](realtimestylus-class.md) 物件傳送的手寫筆向下、封包和手寫筆的通知。 此程式碼應儲存畫筆資料，並建立和儲存筆劃。

如需這類應用程式的範例，請參閱 [ [RealTimeStylus 筆墨收集範例](realtimestylus-ink-collection-sample.md) ] 範例。

> [!Note]  
> 發生 [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) 事件時，請在 DisplaySettingsChanged 事件處理常式中呼叫所收集之筆劃的 [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) 方法，以重新計算 [寬度](/previous-versions/ms582112(v=vs.100)) 和 [高度](/previous-versions/ms582106(v=vs.100)) 屬性。 這是考慮 DisplaySettingsChanged 事件所產生的每一英寸可能點 (DPI) 變更的必要專案。

 

## <a name="ink-collection-and-recognizers"></a>筆墨集合和辨識器

筆墨分析和手寫辨識都不是 [**RealTimeStylus**](realtimestylus-class.md) 物件的功能。 當筆墨收集器外掛程式收集筆墨或您想要辨識筆墨時，您可以將筆墨複製到 [RecognizerCoNtext](/previous-versions/ms552546(v=vs.100)) 或 [分隔](/previous-versions/ms583616(v=vs.100)) 物件。 如需辨識和筆跡分析的詳細資訊，請參閱 [關於手寫辨識](about-handwriting-recognition.md) 或 [分隔物件](the-divider-object.md)。

## <a name="static-rendering"></a>靜態呈現

若要在收集時轉譯筆墨，請將 [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) 物件附加至 [**RealTimeStylus**](realtimestylus-class.md) 物件。 若要在收集筆墨之後轉譯筆墨，請使用轉譯 [器物件將](/previous-versions/ms552630(v=vs.100)) 筆劃繪製至適當的 [圖形](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) 物件。 如需 DynamicRenderer 物件的詳細資訊，請參閱動態轉譯器 [外掛程式](dynamic-renderer-plug-ins.md)。如需靜態和動態轉譯的範例，請參閱 [RealTimeStylus 筆墨收集範例](realtimestylus-ink-collection-sample.md)。

 

 
