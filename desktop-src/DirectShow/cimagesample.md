---
description: CImageSample 類別會執行媒體範例，以管理與 GDI 裝置無關的點陣圖 (DIB) 。
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: 'CImageSample 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afd19b6aba7546ec420985adf6d58d3f7acc7546913ec8f1c168c80ad3b7ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402403"
---
# <a name="cimagesample-class"></a>CImageSample 類別

![cimagesample 類別階層](images/wutil03.png)

`CImageSample`類別會執行媒體範例，以管理與 GDI 裝置無關的點陣圖 (DIB) 。 這個類別衍生自 [**CMediaSample**](cmediasample.md) 類別。 其目的是要搭配 [**CImageAllocator**](cimageallocator.md) 類別使用。 **CImageAllocator** 類別會提供可建立物件的配置器 `CImageSample` 。



| 受保護的成員變數                        | 描述                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**m \_ DibData**](cimagesample-m-dibdata.md)      | 包含此物件正在管理之 DIB 的相關資訊。  |
| [**m \_ bInit**](cimagesample-m-binit.md)          | 指出物件是否已初始化。                |
| 公用方法                                    | 描述                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | 函式方法。                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | 抓取此物件正在管理的 DIB 相關資訊。 |
| [**SetDIBData**](cimagesample-setdibdata.md)     | 設定此物件正在管理的 DIB 相關資訊。      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




