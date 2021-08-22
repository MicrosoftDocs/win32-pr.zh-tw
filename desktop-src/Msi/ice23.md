---
description: ICE23 會驗證每個對話方塊的控制項定位順序。
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbab2d50c07fce208edc845e64cff0061f513c102a55da2d56b49c4a4c17e867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528998"
---
# <a name="ice23"></a>ICE23

ICE23 會驗證每個對話方塊的控制項定位順序。

ICE23 會驗證 [對話方塊資料表](dialog-table.md) 和 [控制資料表](control-table.md)中的下列各項：

-   對話方塊資料表中的每一筆記錄都會指定控制項第一個資料行中的控制項，該控制項 \_ 存在於對話方塊資料行所指定的對話方塊中。
-   控制資料表中的每一筆記錄都會指定控制項下一個資料行中的控制項，該控制項位於與 \_ 控制項資料行中所列控制項相同的對話方塊上，或控制項 \_ 下一個包含 Null 值。
-   在控制 \_ 資料表中，控制下一個控制項的下一個專案之後，會產生單一、關閉的迴圈，並傳回初始控制項。 並非每個控制項都必須在迴圈中，但迴圈必須通過控制項下一個資料行中有專案的每個控制項 \_ 。

## <a name="result"></a>結果

如果控制項的定位順序未在對話方塊中形成單一封閉迴圈，ICE23 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE23 會針對所顯示的範例張貼下列錯誤訊息。

-   Dialog1 沒有先有控制權 \_ 。
-   \_對話方塊 Dialog2 的第一個控制項參考不存在的控制項 ControlX。
-   Dialog3 在控制項 ControlB 中有不正確結束定位順序。
-   Dialog4 在控制項 ControlC 有格式不正確的定位順序
-   Dialog5 在控制項 ControlC 上的定位順序格式錯誤。
-   控制 \_ 控制項 Dialog6 的下一個。 ControlC 連結至未知的控制項。

[對話方塊資料表](dialog-table.md) (部分) 



| 對話  | \_先控制項 |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | ControlX       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[控制資料表](control-table.md) (部分) 



| 對話  | 控制  | 控制 \_ 下一步 |
|---------|----------|---------------|
| Dialog1 | ControlA |               |
| Dialog1 | ControlB | ControlA      |
| Dialog2 | ControlA | ControlB      |
| Dialog2 | ControlB | ControlA      |
| Dialog3 | ControlA | ControlB      |
| Dialog3 | ControlB |               |
| Dialog4 | ControlA | ControlB      |
| Dialog4 | ControlB | ControlC      |
| Dialog4 | ControlC | ControlB      |
| Dialog5 | ControlA | ControlB      |
| Dialog5 | ControlB | ControlC      |
| Dialog5 | ControlC | ControlA      |
| Dialog5 | ControlD | ControlA      |
| Dialog6 | ControlA | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | ControlD | ControlA      |



 

若要修正這些錯誤，請注意上述表格中的下列各項，並進行指定的變更。

並非對話方塊資料表中的每個資料列都有控制項第一個資料行中指定的控制項 \_ 。 將 \_ 對話方塊資料表中 Dialog1 記錄的控制項第一個資料行變更為存在於 Dialog1 中的控制項。

並非對話方塊資料表中的每個資料列都有在對話方塊的控制項第一個資料行中指定的控制項 \_ 。 將 Dialog2 的 Control \_ First 資料行變更為存在於 Dialog2 中的控制項。

將 control 資料表中的 \_ 下一個控制項下的專案控制從控制項變更為，並不會在每一種情況下都進行關閉迴圈。 將 \_ Dialog3 中 ControlB 的 [下一欄] 控制項變更為 ControlA。

將 control 資料表中的 \_ 下一個專案從 control 控制項移至 control 之後，不會在每個案例中導致初始控制項。 將 \_ Dialog4 中 ControlC 的 [控制項下一欄] 變更為參考 ControlA。

將 control 資料表中的下一個專案從 control 控制項下，控制項中的 \_ 下一個專案不會通過控制項下一個資料行中具有專案的對話方塊中的每個控制項 \_ 。 將 \_ Dialog5 中 ControlC 的 [下一欄] 控制項變更為 ControlD。

[ \_ 下一步] 不是指與控制項資料行中所列控制項位於相同對話方塊中的有效控制項。 將 \_ Dialog6 中 ControlC 的 [控制項下一欄] 變更為參考 ControlD。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



