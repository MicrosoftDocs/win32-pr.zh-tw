---
description: 使用手勢的總覽。
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: 使用手勢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c4748dbf2638a57e005562fdec735ea6e87c27757d46549b7577f3bed7741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449243"
---
# <a name="using-gestures"></a>使用手勢

Tablet PC 平臺提供 Microsoft 手勢辨識器，可支援應用程式手勢。 如需 Microsoft 手勢辨識器所支援的手勢清單，請參閱 [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉中的應用程式手勢表格。 Tablet PC 也支援系統手勢。 如需 Tablet PC 支援的系統筆勢清單，請參閱 [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) 列舉中的系統手勢表格。

## <a name="microsoft-gesture-recognizer"></a>Microsoft 手勢辨識器

您可以使用 [**InkCollector**](inkcollector-class.md)物件的 [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)屬性、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control-reference.md)控制項來採用 Microsoft 手勢辨識器。 將 **CollectionMode** 屬性設定為混合模式 (**InkAndGesture**) 或僅限手勢模式 (**GestureOnly**) 預設會將筆墨傳遞給 Microsoft 手勢辨識器。 您可以將 [ [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) ] 屬性設定為 [ **InkAndGesture**]，以搭配 [InkEdit](inkedit-control-reference.md)控制項來使用 Microsoft 手勢辨識器。 您也可以藉由將 [**GestureRecognizer**](gesturerecognizer-class.md)物件新增至其中一個外掛程式集合，來搭配使用手勢辨識和 [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)物件。

但是，如果目前的 Microsoft 手勢辨識器版本不支援您想要使用的手勢，您可以建立自己的辨識器，並將它與 Microsoft 手勢辨識器搭配使用。 這可讓您在應用程式中完整支援筆勢。

Tablet PC 針對部分或所有輸入使用畫筆。 這可讓您輕鬆地撰寫筆跡。 Tablet PC 平臺提供可支援各項手勢分層結構的手寫筆輸入架構。 您可以定義手勢和對應，讓使用者在新的表面上撰寫和叫用先進的手勢，同時保留可叫用其他 Windows 型應用程式之傳統滑鼠訊息的手勢。

Tablet PC 平臺導入了兩個層級的手勢：系統手勢，也稱為系統事件和應用程式手勢。 畫筆架構支援系統和應用程式手勢。 支援單筆觸和多筆觸應用程式手勢。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式手勢](application-gestures.md)
</dt> <dt>

[筆觸手勢](flicks-gestures.md)
</dt> <dt>

[系統手勢](system-gestures.md)
</dt> </dl>

 

 



