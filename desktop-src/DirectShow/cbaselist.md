---
description: CBaseList 方法會執行 abtract 清單。 衍生自 CBaseList 的 CGenericList 類別樣板提供型別檢查和比 CBaseList 類別更簡單的介面。
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: 'CBaseList 類別 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983985"
---
# <a name="cbaselist-class"></a>CBaseList 類別

![cbaselist 類別階層](images/list01.png)

**CBaseList** 方法會執行 abtract 清單。 衍生自 **CBaseList** 的 [**CGenericList**](cgenericlist.md)類別樣板提供型別檢查和比 **CBaseList** 類別更簡單的介面。

**CBaseList** 類別會在 MFC) 程式庫的 Microsoft Foundation (類別中的 **CObList** 類別之後進行模型化。 清單中的位置會以位置結構表示。 呼叫端不應該存取位置結構的內部成員;將它視為清單節點的指標。 物件在清單中的位置會維持有效，直到刪除物件為止。

此清單不需要其所包含物件的任何支援。 它不會在物件上執行任何儲存管理或複製。 物件可以位於多個清單中。

此類別中大約有一半的方法會在單一物件上作用。 這些方法在方法名稱中有尾碼-I。 其他方法會對整個清單採取行動。 例如， [**CBaseList：： AddAfter**](cbaselist-addafter.md) 方法會將清單附加至另一個清單。 單一物件作業會傳回位置值，或在失敗時傳回 **Null** 。 如果成功，則清單作業會傳回 **TRUE** ，否則會傳回 **FALSE** 。



| 受保護的成員變數                             | Description                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**m \_ 計數**](cbaselist-m-count.md)                  | 清單中的專案數。                                              |
| [**m \_ pFirst**](cbaselist-m-pfirst.md)                | 清單中第一個節點的指標。                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | 清單中最後一個節點的指標。                                     |
| 保護方法                                      | Description                                                               |
| [**GetNextI**](cbaselist-getnexti.md)                 | 抓取指定位置的專案，並將位置往前移。  |
| [**GetI**](cbaselist-geti.md)                         | 在指定位置抓取專案。                             |
| [**FindI**](cbaselist-findi.md)                       | 抓取保留指定專案的第一個位置。               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | 移除清單中的第一個專案。                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | 移除清單中的最後一個專案。                                        |
| [**RemoveI**](cbaselist-removei.md)                   | 移除位於指定位置的專案。                               |
| [**AddTailI**](cbaselist-addtaili.md)                 | 將專案加入至清單結尾。                                      |
| [**AddHeadI**](cbaselist-addheadi.md)                 | 將專案加入至清單的前方。                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | 將專案插入指定的位置之後。                             |
| [**AddBeforeI**](cbaselist-addbeforei.md)             | 在指定的位置之前插入專案。                            |
| 公用方法                                         | Description                                                               |
| [**CBaseList**](cbaselist-cbaselist.md)               | 函式方法。                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | 函式方法。                                                        |
| [**RemoveAll**](cbaselist-removeall.md)               | 從清單中移除所有節點。                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | 抓取清單中第一個專案的位置。                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | 抓取清單最後一個專案的位置。                      |
| [**GetCountI**](cbaselist-getcounti.md)               | 捕獲清單中的專案數。                                |
| [**下一步**](cbaselist-next.md)                         | 抓取清單中的下一個位置。                                  |
| [**昨日**](cbaselist-prev.md)                         | 抓取清單中先前的位置。                              |
| [**AddHead**](cbaselist-addhead.md)                   | 將另一個清單插入此清單的前面。                           |
| [**AddTail**](cbaselist-addtail.md)                   | 將另一個清單附加至這份清單的結尾。                             |
| [**AddAfter**](cbaselist-addafter.md)                 | 在指定的位置之後插入清單。                              |
| [**AddBefore**](cbaselist-addbefore.md)               | 在指定的位置之前插入清單。                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | 分割清單，並將標頭部分附加至另一個清單的結尾。 |
| [**MoveToHead**](cbaselist-movetohead.md)             | 分割清單，並將結尾部分插入另一個清單的開頭。 |
| [**反向**](cbaselist-reverse.md)                   | 反轉清單的順序。                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 基類](directshow-base-classes.md)
</dt> </dl>

 

 




