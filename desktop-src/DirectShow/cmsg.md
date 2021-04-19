---
description: CMsgThread 類別支援工作者執行緒，要求可以用非同步方式張貼，而不是直接傳送。
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMsg 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972311"
---
# <a name="cmsg-class"></a>CMsg 類別

[**CMsgThread**](cmsgthread.md)類別支援工作者執行緒，要求可以用非同步方式張貼，而不是直接傳送。 [**CAMThread**](camthread.md)類別提供可傳送單一要求的工作者執行緒。 一次只能有一個用戶端提出要求，而用戶端會封鎖，直到工作者執行緒完成要求為止。 相反地， **CMsgThread** 類別會提供可以張貼任意數量要求的工作者執行緒。 以物件) 形式 (的要求 `CMsg` 會以非同步方式排入佇列並依序執行。 未收到回復或傳回值。



| 資料成員              | Description                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | 要求碼的旗標參數。                                                                                                                                               |
| lpParam                   | 背景工作執行緒所需的資料做為參數或傳回值。 此資料不應以堆疊為基礎，因為它會在完成佇列作業之後被參考一段時間。 |
| pEvent                    | 背景工作執行緒可以指示的事件物件，表示作業已完成。                                                                                         |
| uMsg                      | 由執行緒類別的用戶端所定義，且由覆寫的背景工作執行緒函數所瞭解的要求程式碼。                                                           |
| 成員函數          | Description                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | 結構 [**CMsg**](cmsg-cmsg.md) 物件。                                                                                                                                    |



 

 

 



