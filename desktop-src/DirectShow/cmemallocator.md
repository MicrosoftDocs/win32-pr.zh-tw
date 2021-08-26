---
description: 執行支援 IMemAllocator 介面的配置器。
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: 'CMemAllocator 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915928"
---
# <a name="cmemallocator-class"></a>CMemAllocator 類別

![cmemallocator 類別階層](images/filter10.png)

執行支援 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的配置器。

這個類別衍生自 [**CBaseAllocator**](cbaseallocator.md)。 如需配置器的詳細資訊，請參閱 [**CBaseAllocator**](cbaseallocator.md)的檔。



| 受保護的成員變數                              | 描述                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pBuffer**](cmemallocator-m-pbuffer.md)           | 包含緩衝區之記憶體區塊的指標。                   |
| 保護方法                                       | 描述                                                              |
| [**自由**](cmemallocator-free.md)                      | 預留位置方法;在取消認可操作期間呼叫。                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | 釋放緩衝區的記憶體。                                     |
| [**配置**](cmemallocator-alloc.md)                    | 配置緩衝區的記憶體。                                        |
| 公用方法                                          | 描述                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | 函式方法。                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | 函式方法。                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | 建立 **CMemAllocator** 類別的新實例。                   |
| IMemAllocator 方法                                   | 描述                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | 指定要配置的緩衝區數目和每個緩衝區的大小。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[提供自訂配置器](providing-a-custom-allocator.md)
</dt> </dl>

 

 




