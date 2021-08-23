---
description: ITCallQualityControl 介面會公開方法，讓應用程式取得和設定通話品質控制的參數。
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: 'ITCallQualityControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb31452f6f4693e8bfbf725a5ddae7d7305868c2603806895c98e16df4d3e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061006"
---
# <a name="itcallqualitycontrol-interface"></a>ITCallQualityControl 介面

\[這個介面無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

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
| [**設置**](itcallqualitycontrol-set.md)           | 設定指定之 [通話品質控制項屬性](callqualityproperty.md)的值。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

