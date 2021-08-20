---
title: IReferenceClock 介面
description: IReferenceClock 介面提供外部時鐘的存取。 提供此介面可讓所有轉譯常式同步處理至相同的時鐘。您可以從 reader 物件取得這個介面。
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- IReferenceClock 介面 windows 媒體格式
- IReferenceClock 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97f3d84dbb04de8d8b7fa297e9547ed628f7bf340360c6d5309ddaf8f96eb351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655175"
---
# <a name="ireferenceclock-interface"></a>IReferenceClock 介面

**IReferenceClock** 介面提供外部時鐘的存取。 提供此介面可讓所有轉譯常式同步處理至相同的時鐘。

您可以從 reader 物件取得這個介面。

## <a name="members"></a>成員

**IReferenceClock** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IReferenceClock** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IReferenceClock** 介面具有這些方法。



| 方法                                                   | 描述                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**AdvisePeriodic**](ireferenceclock-adviseperiodic.md) | 未由此 SDK 所執行。<br/>                                   |
| [**AdviseTime**](ireferenceclock-advisetime.md)         | 要求經過一段時間的非同步通知。<br/> |
| [**GetTime**](ireferenceclock-gettime.md)               | 抓取目前的參考時間。<br/>                          |
| [**Unadvise**](ireferenceclock-unadvise.md)             | 取消通知要求。<br/>                                |



 

## <a name="remarks"></a>備註

如需可以使用此介面的 QueryInterface 方法取得之其他介面的詳細資訊，請參閱 Reader 物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](interfaces.md)
</dt> </dl>

 

