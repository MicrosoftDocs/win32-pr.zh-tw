---
description: CBaseRendererInputPin 類別會為 CBaseRenderer 類別實作為輸入的 pin。 除非另有說明，否則這個類別中的方法會委派至 CBaseRenderer 類別上的對應方法。
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: 'CRendererInputPin 類別 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2cfeb61d075804d61ba515d86641e56bf3cd9e1ab6aa6de826a8bb7206be4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908241"
---
# <a name="crendererinputpin-class"></a>CRendererInputPin 類別

![crendererinput 釘選類別階層](images/rbase01.png)

**CBaseRendererInputPin** 類別會為 [**CBaseRenderer**](cbaserenderer.md)類別實作為輸入的 pin。 除非另有說明，否則這個類別中的方法會委派至 **CBaseRenderer** 類別上的對應方法。



| 受保護的成員變數                                       | 描述                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pRenderer**](crendererinputpin-m-prenderer.md)            | 篩選準則的指標。                                                                 |
| 公用方法                                                   | 描述                                                                            |
| [**CRendererInputPin**](crendererinputpin-crendererinputpin.md) | 函式方法。                                                                    |
| [**BreakConnect**](crendererinputpin-breakconnect.md)           | 在中斷連接時新增自訂程式碼。                                       |
| [**CompleteConnect**](crendererinputpin-completeconnect.md)     | 完成連接。                                                              |
| [**CheckMediaType**](crendererinputpin-checkmediatype.md)       | 判斷 pin 是否可以支援特定的媒體類型。                               |
| [**使用中**](crendererinputpin-active.md)                       | 將釘選切換為作用中的 (已暫停或正在執行) 模式。                               |
| [**非使用中**](crendererinputpin-inactive.md)                   | 將釘選切換為非使用中狀態，並釋放配置器的記憶體。        |
| [**SetMediaType**](crendererinputpin-setmediatype.md)           | 設定釘選的媒體類型。                                                        |
| [**分配器**](crendererinputpin-allocator.md)                 | 捕獲預設記憶體配置器的指標。                                   |
| IPin 方法                                                     | 描述                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | 抓取 pin 的識別碼。                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | 通知 pin，在發出新的執行命令之前，不需要額外的資料。 |
| [**BeginFlush**](crendererinputpin-beginflush.md)               | 通知 pin 開始進行清除作業。                                            |
| [**EndFlush**](crendererinputpin-endflush.md)                   | 通知 pin 結束清除作業。                                              |
| IMemInputPin 方法                                             | 描述                                                                            |
| [**收到**](crendererinputpin-receive.md)                     | 從資料流程抓取下一個資料區塊。                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




