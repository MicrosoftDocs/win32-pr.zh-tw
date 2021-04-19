---
description: XAPO API 可讓您建立跨平臺音訊處理物件 (XAPO) ，以在 Windows 和 Xbox 360 的 XAudio2 中使用。
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: XAPO 概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975327"
---
# <a name="xapo-overview"></a>XAPO 概觀

XAPO API 可讓您建立跨平臺音訊處理物件 (XAPO) ，以在 Windows 和 Xbox 360 的 XAudio2 中使用。 XAPO 是接受傳入音訊資料的物件，並在資料傳遞之前對資料執行某些作業。 您可以使用 XAPO 來執行各種不同的工作，包括將回音新增至音訊串流以及監視尖峰音量層級。

## <a name="creating-new-xapos"></a>建立新的 XAPOs

XAPO API 會提供 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面和 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 類別來建立新的 XAPO 類型。 **IXAPO** 介面包含所有需要實作為建立新 XAPO 的方法。 **CXAPOBase** 類別提供 **IXAPO** 介面的基本實作為。 **CXAPOBase** 會執行所有 **IXAPO** 介面方法，但是 [**IXAPO：:P ROCESS**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法是每個 XAPO 唯一的。

如需建立新 XAPO 的範例，請參閱 [如何：建立 XAPO](how-to--create-an-xapo.md)。

如需建立接受執行時間參數之 XAPO 的範例，請參閱 [如何：將執行時間參數支援加入至 XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md)。

## <a name="xapos-and-com"></a>XAPOs 和 COM

XAPOs 會執行 **IUnknown** 介面。 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)和 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)介面包括三個 **IUnknown** 方法： **QueryInterface**、 **AddRef** 和 **Release**。 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 提供這三種 IUnknown 方法的所有方法。 **CXAPOBase** 的新實例會有1的參考計數。 當其參考計數變成0時，就會將它終結。 **IXAPO** 和 **IXAPOParameters** 的執行應該遵循相同的模式，以便在與 XAudio2 搭配使用時，能夠適當地進行管理。

XAPO 實例會以 **IUnknown** 介面的形式傳遞至 XAudio2。 XAudio2 會使用 **QueryInterface** 來取得 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面，以及偵測 XAPO 是否會實作為 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) 介面。 **IXAPO** 的執行必須接受 **\_ \_ uuidof (IXAPO)** 的要求。 如果 **IXAPOParameters** 已實作為，它也必須接受 **\_ \_ uuidof (IXAPOParameters)** 的要求。

## <a name="using-an-xapo-in-xaudio2"></a>在 XAudio2 中使用 XAPO

XAPOs 會在 XAudio2 中使用，方法是將它們附加至語音。 每個 XAudio2 voice 都有一個效果鏈，其中包含零或多個音訊效果。 傳送至語音的音訊資料會在傳送到語音輸出目標之前通過鏈中的每個效果。 使用 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)方法的 *pInputProcessParameters* 參數，將資料從語音傳遞到每個效果。 然後使用 *pOutputProcessParameters* 參數將它傳回給語音。 語音會取得每個效果的輸出，然後將其送入鏈中的下一個效果，直到鏈中沒有任何效果。

如需 XAudio2 效果鏈的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md)。

如需在 XAudio2 中使用 XAPO 的範例，請參閱 how [to：使用 XAudio2 中的 XAPO](how-to--use-an-xapo-in-xaudio2.md)。

## <a name="effect-libraries"></a>效果程式庫

XAPO 效果程式庫包含數個 XAPOs，以及用來具現化它們的常用方法。 如需 XAPOFX 的詳細資訊，請參閱 [XAPOFX 總覽](xapofx-overview.md) 。 此外，XAudio2 也有內建的「回音」和「大量計量」效果。 如需內建 XAudio2 效果的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAudio2 音訊效果](xaudio2-audio-effects.md)
</dt> </dl>

 

 
