---
description: CImageAllocator 類別會執行管理與 GDI 裝置無關點陣圖 (Dib) 的配置器。 這個類別衍生自 CBaseAllocator 類別。 它會建立使用 CImageSample 類別所執行的媒體範例。
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: 'CImageAllocator 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989710"
---
# <a name="cimageallocator-class"></a>CImageAllocator 類別

![cimageallocator 類別階層](images/wutil04.png)

`CImageAllocator`類別會執行管理與 GDI 裝置無關點陣圖 (dib) 的配置器。 這個類別衍生自 [**CBaseAllocator**](cbaseallocator.md) 類別。 它會建立使用 [**CImageSample**](cimagesample.md) 類別所執行的媒體範例。

配置器是由兩個連接的 pin 所共用，但一律由連接中的其中一個篩選準則所擁有。 使用的篩選準則必須追蹤配置器 `CImageAllocator` 是否由本身或其他篩選器提供。 如果配置器是由本身提供的，則擁有篩選器可以依賴配置器的所有媒體範例都是 **CImageSample** 物件的事實。 因此，它可以使用 **CImageSample** 物件來取得 DIB （儲存在 [**DIBDATA**](dibdata.md) 結構中）的相關資訊。

當媒體類型變更時，擁有篩選應呼叫 **NotifyMediaType** 。



| 受保護的成員變數                                     | Description                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | 擁有篩選準則的指標。                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | 目前媒體類型的指標。                                       |
| 保護方法                                              | Description                                                              |
| [**配置**](cimageallocator-alloc.md)                         | 配置緩衝區的記憶體。                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | 針對目前的媒體類型檢查配置器屬性。              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | 建立 DIB。                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | 建立媒體範例。 虛擬。                                         |
| [**免費**](cimageallocator-free.md)                           | 釋放所有緩衝區記憶體。                                       |
| 公用方法                                                 | Description                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | 函式方法。                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | 通知物件目前的媒體類型。                            |
| IMemAllocator 方法                                          | Description                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | 指定要配置的緩衝區數目和每個緩衝區的大小。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




