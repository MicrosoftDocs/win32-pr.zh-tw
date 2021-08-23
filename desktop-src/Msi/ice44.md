---
description: ICE44 會驗證 NewDialog、SpawnDialog 和 SpawnWaitDialog 的事件，會在對話方塊資料表中參考有效的對話方塊。
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ee7bb074ec2dcc395cdf17750e2ab1b0364026e0f949c9b9e3f2589a8b59261
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581008"
---
# <a name="ice44"></a>ICE44

ICE44 會驗證 [NewDialog](newdialog-controlevent.md)、 [SpawnDialog](spawndialog-controlevent.md)和 [SpawnWaitDialog](spawnwaitdialog-controlevent.md) 的事件，會在 [對話方塊資料表](dialog-table.md)中參考有效的對話方塊。

## <a name="result"></a>結果

如果有對話方塊控制項事件未參考對話方塊資料表中所列的對話方塊，ICE44 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE44 會針對所顯示的範例報告下列錯誤。



| ICE44 錯誤                                                                                                                               | 描述                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 控制項 ' Dialog1 ' 的控制項事件。Control1 ' 的類型為 SpawnDialog，但其引數 Dialog2 不是對話方塊資料表中的有效專案。 | 有 SpawnDialog、SpawnWaitDialog 或 NewDialog 動作具有未參考對話方塊資料表中對話方塊的引數。 若要修正這個錯誤，請在對話方塊資料表中新增一個索引鍵的引數。<br/> |



 

[對話方塊資料表](dialog-table.md) (部分) 



| 對話  | 標題 |
|---------|-------|
| Dialog1 |       |



 

[ControlEvent 資料表](controlevent-table.md) (部分) 



| 對話\_ | 控制項\_ | 類型        | 引數 |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




