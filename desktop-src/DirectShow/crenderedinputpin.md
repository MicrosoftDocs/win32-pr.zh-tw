---
description: CRenderedInputPin 類別是用來在轉譯器上執行輸入釘選的基類。
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: 'CRenderedInputPin 類別 (Amextra) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 139b0ebd887dc81efd19953d48f3caa8fd6377acde8723de23178ee7a0278c8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585291"
---
# <a name="crenderedinputpin-class"></a>CRenderedInputPin 類別

![crenderedinputpin 類別階層](images/rbase04.png)

**CRenderedInputPin** 類別是用來在轉譯器上執行輸入釘選的基類。 這個類別是針對並非衍生自 [**CBaseRenderer**](cbaserenderer.md) 類別的轉譯器篩選所設計。  (衍生自 **CBaseRenderer** 的篩選器應該使用輸入 Pin 的 [**CRendererInputPin**](crendererinputpin.md) 類別。 ) 

若要使用這個類別，您必須至少執行下列作業：

-   宣告繼承 **CRenderedInputPin** 的新 pin 類別。
-   在您的 pin 類別中，宣告重要區段物件以保存串流鎖定。 您可以針對此用途使用 [**CCritSec**](ccritsec.md) 類別。 如需詳細資訊，請參閱 [執行緒和重要區段](threads-and-critical-sections.md)。
-   覆寫 [**CRenderedInputPin：： EndOfStream**](crenderedinputpin-endofstream.md) 以保存串流鎖定。
-   執行 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)、 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md)和 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法。
-   在篩選準則中，請執行 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 來傳回您的 pin 類別的實例。

您可以在具有多個輸入釘選的轉譯器中使用這個類別。 此類別會繼承 [**CBaseInputPin**](cbaseinputpin.md) 類別。



| 受保護的成員變數                                            | 描述                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**m \_ bAtEndOfStream**](crenderedinputpin-m-batendofstream.md)       | 指出是否已到達資料流程的結尾。                                                         |
| [**m \_ bCompleteNotified**](crenderedinputpin-m-bcompletenotified.md) | 指出 pin 是否已將 [**EC \_ 完成**](ec-complete.md)事件傳送至篩選 Graph 管理員。 |
| 公用方法                                                        | 描述                                                                                                  |
| [**使用中**](crenderedinputpin-active.md)                            | 通知釘選篩選現在已啟用。                                                              |
| [**CRenderedInputPin**](crenderedinputpin-crenderedinputpin.md)      | 函式方法。                                                                                          |
| [**執行**](crenderedinputpin-run.md)                                  | 通知釘選篩選現在正在執行。                                                             |
| IPin 方法                                                          | 描述                                                                                                  |
| [**EndFlush**](crenderedinputpin-endflush.md)                        | 結束清除操作。                                                                                      |
| [**EndOfStream**](crenderedinputpin-endofstream.md)                  | 通知 pin，在篩選器收到新的執行命令之前，不需要額外的資料。            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amextra (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




