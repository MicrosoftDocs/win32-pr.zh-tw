---
description: 以媒體會話使用媒體來源
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: 以媒體會話使用媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945634"
---
# <a name="using-media-sources-with-the-media-session"></a>以媒體會話使用媒體來源

如果您使用媒體會話來控制播放，您應該在媒體來源上呼叫的一組方法會受到限制。 本節說明如何搭配媒體會話使用媒體來源。

以下是您的應用程式將執行的基本步驟：

1.  建立媒體來源。 若要建立媒體來源，請使用來源解析程式。 如需詳細資訊，請參閱 [來源解析程式](source-resolver.md)。 來源解析程式會傳回來源 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。  (如果您已經撰寫自訂媒體來源，則可以改為提供自訂的建立方法。 ) 

2.  設定簡報。 若要設定來源的簡報，請呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)。 您可以修改此複本，但在播放開始之前，這些變更不會變成作用中狀態。 播放期間請勿修改簡報描述項。 如需詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。

3.  建立包含媒體來源的拓撲。 如需詳細資訊，請參閱 [拓撲](topologies.md)。

4.  使用媒體會話來控制播放。 媒體會話會呼叫媒體來源上的方法。 應用程式目前不應呼叫媒體來源上的任何方法。

5.  釋放媒體來源之前，請呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 以關閉來源。

    > [!Note]  
    > 如果您使用 sequencer 來源，sequencer 來源會處理關閉區段來源的工作。 如需詳細資訊，請參閱 [Sequencer 來源](sequencer-source.md)。

     

如果您使用媒體會話，您應該在媒體來源上呼叫的唯一方法是 [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)、 [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)和 [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)。 尤其是：

-   請勿呼叫 [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)、 [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)或 [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop);這些方法只能由媒體會話呼叫。

-   請勿呼叫任何 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 方法。

-   請勿直接從媒體來源或任何資料流程取得事件。 媒體會話必須接收這些事件，管線才能正常運作。 媒體會話轉送應用程式所需的任何事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> </dl>

 

 



