---
description: ITStreamQualityControl 會公開方法，讓應用程式取得和設定 stream 品質控制項的參數。
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: 'ITStreamQualityControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990667"
---
# <a name="itstreamqualitycontrol-interface"></a>ITStreamQualityControl 介面

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。 RTC 用戶端 API 提供類似的功能。\]

**ITStreamQualityControl** 會公開方法，讓應用程式取得和設定 stream 品質控制項的參數。

此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。 只有在呼叫使用這些服務提供者時，才會公開此服務提供者。

## <a name="members"></a>成員

**ITStreamQualityControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITStreamQualityControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITStreamQualityControl** 介面具有這些方法。



| 方法                                              | 描述                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**獲取**](itstreamqualitycontrol-get.md)           | 取得指定之 [資料流程品質屬性](streamqualityproperty.md)的值。<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | 取得指定之 [資料流程品質屬性](streamqualityproperty.md)的有效值範圍。<br/> |
| [**設定**](itstreamqualitycontrol-set.md)           | 設定指定之 [資料流程品質屬性](streamqualityproperty.md)的值。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

