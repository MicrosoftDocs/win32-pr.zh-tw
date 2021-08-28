---
description: 資料流程屬性
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: 資料流程屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d066520926363b27ed5f29e29079d960a0f8e1e395c3dc0df56af918b5fed34a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034726"
---
# <a name="stream-attributes"></a>資料流程屬性

下列屬性適用于媒體資料流程。 若要從媒體範例取得屬性，請使用 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 方法。



| 屬性                                                                                   | 描述                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [MFStreamExtension \_ CameraExtrinsics](mfstreamextension-cameraextrinsics.md)               | 資料流程的相機 extrinsics。         |
| [MFStreamExtension \_ PinholeCameraIntrinsics](mfstreamextension-pinholecameraintrinsics.md) | 資料流程的 pinhole 攝影機內建函式。 |



 

並非每個媒體資料流程都包含此處所列的每個屬性。 在某些情況下，屬性只適用于特定類型的資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 



