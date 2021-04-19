---
description: IH323LineEx 介面是由 H323 MSP 所執行，而且僅適用于 .H 位址物件。 此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: 'IH323LineEx 介面 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992991"
---
# <a name="ih323lineex-interface"></a>IH323LineEx 介面

\[**IH323LineEx** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**IH323LineEx** 介面是由 [H323 MSP](h323-msp.md)所執行，而且僅適用于 .h 位址物件。 此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。

> [!Note]  
> 此介面中的所有方法都應該只在註冊此位址的撥入電話之後呼叫。

 

## <a name="members"></a>成員

**IH323LineEx** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IH323LineEx** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IH323LineEx** 介面具有這些方法。



| 方法                                                                                 | 描述                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | 為位址設定預設的 H. 323 別名。<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | 設定預設功能的喜好設定加權。<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | 為數據交換設定外部的 T. 120 位址。<br/>       |



 

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

 

