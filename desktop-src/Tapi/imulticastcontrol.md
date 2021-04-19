---
description: IMulticastControl 介面是由 IPConf MSP 所執行，而且僅適用于多播呼叫物件。
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: 'IMulticastControl 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993222"
---
# <a name="imulticastcontrol-interface"></a>IMulticastControl 介面

\[**IMulticastControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**IMulticastControl** 介面是由 IPConf MSP 所執行，而且僅適用于多播呼叫物件。 此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。 **IMulticastControl** 介面控制多播回送模式。

在 MM \_ NO \_ 回送模式中，多播回送已停用，這表示同一部電腦上同時加入相同多播群組的兩個應用程式將會取得彼此的封包。 如果一律只有一個應用程式在電腦上加入多播群組，則此模式的效能最佳。 MM \_ 沒有 \_ 預設模式的回送模式。

MM \_ 完整 \_ 回送模式只適用于測試。 送出的所有封包也會回復。 這可以用來測試裝置是否正常運作。

MM \_ 選擇性 \_ 回送模式可用來讓一部電腦上的多個應用程式加入相同的多播群組。 封包會從堆疊環回，且每個 RTP 會話都會負責篩選掉不需要的封包。

## <a name="members"></a>成員

**IMulticastControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IMulticastControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMulticastControl** 介面具有這些方法。



| 方法                                                          | 描述                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**取得 \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | 取得多播回送模式。<br/> |
| [**put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | 設定多播回送模式。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

