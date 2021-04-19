---
description: ITFormatControl 介面會公開方法，以允許應用程式抓取有關呼叫之接收或傳輸資料流程格式的資訊。
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: 'ITFormatControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996254"
---
# <a name="itformatcontrol-interface"></a>ITFormatControl 介面

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。 RTC 用戶端 API 提供類似的功能。\]

**ITFormatControl** 介面會公開方法，以允許應用程式抓取有關呼叫之接收或傳輸資料流程格式的資訊。

此介面是由 [H323 MSP](h323-msp.md) 所執行，而且只會在呼叫使用此服務提供者時公開。

## <a name="members"></a>成員

**ITFormatControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITFormatControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITFormatControl** 介面具有這些方法。



| 方法                                                                     | 描述                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | 取得目前資料流程的媒體格式。<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | 取得與目前格式相關聯的功能數目。<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | 取得與指定之格式索引相關聯的功能。<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | 釋放與格式相關聯的結構。<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | 設定格式功能的新順序。<br/>                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

