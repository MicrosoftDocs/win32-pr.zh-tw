---
description: '[取消] 對話方塊會確認使用者是否想要結束安裝。 這是強制回應對話方塊。'
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: 取消對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2f0ba12c442b8b0f4445077497c26649b79714d1a1d77af7b2a82e6c1a3f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105388"
---
# <a name="cancel-dialog"></a>取消對話方塊

[ **取消** ] 對話方塊會確認使用者是否想要結束安裝。 這是強制回應對話方塊。

這種類型的對話方塊通常包含 [文字控制項](text-control.md) 和兩個 [按鈕](pushbutton-control.md)。 這兩個按鈕可讓使用者選擇返回最後一個對話方塊或確認安裝終止。

[EndDialog](enddialog-controlevent.md) ControlEvent 會連結到[ControlEvent 資料表](controlevent-table.md)中的這兩個按鈕。 EndDialog ControlEvent 的 *Return* 參數會連結到其中一個按鈕，並導致 [ **取消** ] 對話方塊終止，並讓焦點回到上一個對話方塊。 *Exit* 參數會連結至另一個按鈕，並讓使用者介面使用適當的程式碼將控制權傳回給安裝程式，表示使用者想要結束。 然後，安裝程式就會關閉並顯示 [ [UserExit] 對話方塊](userexit-dialog.md)。

 

 



