---
description: ITCallQualityControl 介面會公開方法，讓應用程式取得和設定通話品質控制的參數。
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: 'ITCallQualityControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995938"
---
# <a name="itcallqualitycontrol-interface"></a>ITCallQualityControl 介面

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。 RTC 用戶端 API 提供類似的功能。\]

**ITCallQualityControl** 介面會公開方法，讓應用程式取得和設定通話品質控制的參數。

此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。 只有在呼叫使用這些服務提供者時，才會公開此服務提供者。

## <a name="members"></a>成員

**ITCallQualityControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITCallQualityControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITCallQualityControl** 介面具有這些方法。



| 方法                                            | 描述                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**獲取**](itcallqualitycontrol-get.md)           | 取得指定之 [通話品質控制項屬性](callqualityproperty.md)的值。<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | 取得指定之 [呼叫品質控制項屬性](callqualityproperty.md)的有效值範圍。<br/> |
| [**設定**](itcallqualitycontrol-set.md)           | 設定指定之 [通話品質控制項屬性](callqualityproperty.md)的值。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

