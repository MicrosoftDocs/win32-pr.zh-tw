---
description: IKeyFrameControl 介面是由 h.264 MSP 所執行，而且只能在 h. 資料流程物件上使用。
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: 'IKeyFrameControl 介面 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989659"
---
# <a name="ikeyframecontrol-interface"></a>IKeyFrameControl 介面

\[**IKeyFrameControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**IKeyFrameControl** 介面是由 h.264 [MSP](h323-msp.md)所執行，而且只能在 h. 資料流程物件上使用。 此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。 它有兩種方法可讓應用程式要求遠端端點以主要畫面格更新影片影像。

## <a name="members"></a>成員

**IKeyFrameControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IKeyFrameControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IKeyFrameControl** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**PeriodicUpdatePicture**](ikeyframecontrol-periodicupdatepicture.md) | 設定資料流程中的計時器，以定期要求圖片更新。<br/> |
| [**UpdatePicture**](ikeyframecontrol-updatepicture.md)                 | 要求影片寄件者更新圖片。<br/>                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>H323priv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[H323 MSP](h323-msp.md)
</dt> </dl>

 

