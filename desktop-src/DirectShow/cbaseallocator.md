---
description: CBaseAllocator 類別是一種抽象基類，可實作為配置器。 配置器會公開 IMemAllocator 介面。
ms.assetid: 3c9003d8-f15c-4e85-9712-9aaa87dffdf3
title: 'CBaseAllocator 類別 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 068dd45ee3ffac5c3b915c3b0cdd8bc87756377e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989586"
---
# <a name="cbaseallocator-class"></a>CBaseAllocator 類別

![cbaseallocator 類別階層](images/filter10.png)

**CBaseAllocator** 類別是一種抽象基類，可實作為配置器。 配置器會公開 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。

配置 *器是可* 配置記憶體緩衝區的物件。 配置器會維護可用緩衝區的清單。 當用戶端 (通常是篩選) 要求緩衝區時，配置器會從清單中抓取一個。 用戶端會將資料填滿緩衝區，而且可能會將緩衝區傳遞至另一個物件。 最後會釋出緩衝區，而配置器會將它傳回給可用的緩衝區清單。

每個緩衝區都是由稱為 *媒體範例* 的物件所封裝。 媒體範例是一種將指標封裝至元件物件模型中之記憶體區塊的方式， (COM) 架構。 媒體範例會公開 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面，並且使用 [**CMediaSample**](cmediasample.md) 類別來執行。 媒體範例包含相關緩衝區的指標，可透過呼叫 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 方法來存取。 如需詳細資訊，請參閱 [範例和配置器](samples-and-allocators.md)。

若要使用此類別，請執行下列步驟：

1.  呼叫 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md) 方法來指定緩衝區需求，包括緩衝區數目和每個緩衝區的大小。
2.  呼叫 [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法以配置緩衝區。
3.  呼叫 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法以取得媒體範例。 這個方法會封鎖，直到下一個範例可供使用為止。
4.  當您完成每個範例時，請在範例上呼叫 **IUnknown：： Release** 方法。 當範例的參考計數達到零時，不會刪除此範例。 相反地，此範例會返回配置器的可用清單。
5.  當您完成使用配置器時，請呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 方法來釋放緩衝區的記憶體。

[**Commit**](cbaseallocator-commit.md)方法會呼叫虛擬方法 [**CBaseAllocator：：**](cbaseallocator-alloc.md)配置，以配置緩衝區的記憶體。 [**取消認可**](cbaseallocator-decommit.md)方法會呼叫純虛擬方法 [**CBaseAllocator：： Free**](cbaseallocator-free.md)，這會釋出記憶體。 衍生類別必須覆寫這兩種方法。

[**CMemAllocator**](cmemallocator.md)基類衍生自 **CBaseAllocator**。 篩選基類會使用 **CMemAllocator** 類別。



| 受保護的成員變數                                                   | Description                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**m \_ lFree**](cbaseallocator-m-lfree.md)                                   | 可用 (免費) 媒體範例清單的指標。                                       |
| [**m \_ hSem**](cbaseallocator-m-hsem.md)                                     | 範例變成可用時所發出的信號。                                |
| [**m \_ lWaiting**](cbaseallocator-m-lwaiting.md)                             | 等候樣本的執行緒計數。                                                      |
| [**m \_ lCount**](cbaseallocator-m-lcount.md)                                 | 要提供的緩衝區數目。                                                              |
| [**m \_ lAllocated**](cbaseallocator-m-lallocated.md)                         | 目前配置的緩衝區數目。                                                     |
| [**m \_ lSize**](cbaseallocator-m-lsize.md)                                   | 每個緩衝區的大小。                                                                       |
| [**m \_ lAlignment**](cbaseallocator-m-lalignment.md)                         | 每個緩衝區的對齊方式。                                                                  |
| [**m \_ lPrefix**](cbaseallocator-m-lprefix.md)                               | 每個緩衝區的前置詞。                                                                     |
| [**m \_ bChanged**](cbaseallocator-m-bchanged.md)                             | 指出緩衝區需求是否已變更的旗標。                              |
| [**m \_ bCommitted**](cbaseallocator-m-bcommitted.md)                         | 指出是否已認可配置器的旗標。                                  |
| [**m \_ bDecommitInProgress**](cbaseallocator-m-bdecommitinprogress.md)       | 旗標，指出取消認可作業是否正在進行中。                               |
| [**m \_ pNotify**](cbaseallocator-m-pnotify.md)                               | 回呼介面的指標，會在釋放樣本時呼叫。                |
| [**m \_ fEnableReleaseCallback**](cbaseallocator-m-fenablereleasecallback.md) | 指出是否已啟用發行回呼的旗標。                                   |
| 保護方法                                                            | Description                                                                                |
| [**配置**](cbaseallocator-alloc.md)                                        | 配置緩衝區的記憶體。 虛擬。                                                 |
| 公用方法                                                               | Description                                                                                |
| [**CBaseAllocator**](cbaseallocator-cbaseallocator.md)                      | 函式方法。                                                                        |
| [**~ CBaseAllocator**](cbaseallocator--cbaseallocator.md)                   | 函式方法。                                                                         |
| [**SetNotify**](cbaseallocator-setnotify.md)                                | 已過時。                                                                                  |
| [**GetFreeCount**](cbaseallocator-getfreecount.md)                          | 抓取未使用的媒體樣本數目。                                 |
| [**NotifySample**](cbaseallocator-notifysample.md)                          | 釋放任何正在等候樣本的執行緒。                                         |
| [**SetWaiting**](cbaseallocator-setwaiting.md)                              | 遞增等候中線程的計數。                                                   |
| 純虛擬方法                                                         | Description                                                                                |
| [**自由**](cbaseallocator-free.md)                                          | 釋放所有緩衝區記憶體。                                                         |
| IMemAllocator 方法                                                        | Description                                                                                |
| [**SetProperties**](cbaseallocator-setproperties.md)                        | 指定要配置的緩衝區數目和每個緩衝區的大小。                   |
| [**GetProperties**](cbaseallocator-getproperties.md)                        | 捕獲配置器將建立的緩衝區數目，以及緩衝區屬性。 |
| [**Commit**](cbaseallocator-commit.md)                                      | 配置緩衝區的記憶體。                                                      |
| [**取消認可**](cbaseallocator-decommit.md)                                  | 解除緩衝區。                                                                     |
| [**GetBuffer**](cbaseallocator-getbuffer.md)                                | 抓取包含緩衝區的媒體範例。                                           |
| [**ReleaseBuffer**](cbaseallocator-releasebuffer.md)                        | 將媒體範例傳回到可用媒體範例清單。                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[提供自訂配置器](providing-a-custom-allocator.md)
</dt> </dl>

 

 




