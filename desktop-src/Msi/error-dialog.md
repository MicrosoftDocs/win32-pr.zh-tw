---
description: 錯誤對話方塊是顯示錯誤訊息的強制回應對話方塊。 每個安裝中都可以存在一個以上的錯誤對話方塊。
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: 錯誤對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512161"
---
# <a name="error-dialog"></a>錯誤對話方塊

錯誤對話方塊是顯示錯誤訊息的強制回應對話方塊。 每個安裝中都可以存在一個以上的錯誤對話方塊。

必須設定 ErrorDialog 屬性，以指定要使用哪一個對話方塊。 如果未設定此屬性，或未指向有效的錯誤對話方塊，則不會顯示錯誤訊息。 在此情況下，只會記錄錯誤，並出現關於遺漏對話方塊的警告。

錯誤對話方塊必須設定 [錯誤對話方塊樣式位](error-dialog-style-bit.md) 。 對話方塊必須有一個名為 ErrorText 的 [文字控制項](text-control.md) 。 [對話方塊資料表](dialog-table.md)中錯誤對話方塊的記錄必須在控制項的第一個欄位中輸入 ErrorText 控制項 \_ 。

對話方塊必須包含七個 [按鈕](pushbutton-control.md)。 所有這些按鈕會在[ControlEvent 資料表](controlevent-table.md)中指定[EndDialog](enddialog-controlevent.md) ControlEvent。 每個按鈕都會指定下列其中一個屬性： **ErrorAbort**、 **ErrorCancel**、 **ErrorIgnore**、 **ErrorNo**、 **ErrorOk**、 **ErrorRetry**、 **ErrorYes**。

> [!Note]  
> 這些控制項的焦點不應透過使用 \_ [控制資料表](control-table.md)中的 [下一步] 資料行來連結。

 

這些按鈕的位置應該與對話方塊中的位置大致相同，因為當建立時，根據訊息而定，只會建立這七個按鈕的子集。 按鈕的 X 座標會進行修改，因此顯示的按鈕會平均間距。 按鈕的 Y 座標、高度和寬度都不會變更。 因為按鈕會水準排列，所以不能將其他控制項放在對話方塊的相同水準區域中。

針對錯誤對話方塊， \_ 會忽略對話方塊資料表中的 [控制項預設值] 和 [控制項 \_ 取消 []](dialog-table.md) 欄位。 \_錯誤對話方塊的控制項第一個欄位必須指定 ErrorText 控制項。

如果此對話方塊中包含名為 ErrorIcon 的 [圖示控制項](icon-control.md) ，則會顯示下列標準 Windows 圖示：

-   IDI \_ 錯誤，以回應 imtFatalExit 訊息。
-   IDI \_ 警告以回應 imtError 和 imtWarning 訊息。
-   IDI \_ 資訊以回應 imtOutOfDiskSpace 訊息。

應建立 ErrorIcon 控制項，並設定 [FixedSize control 屬性](fixedsize-control-attribute.md) ，以避免標準 Windows 圖示的大小不適當。

 

 



