---
description: 描述如何搭配使用 PenInputPanel 物件與下拉式方塊。
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: 使用 PenInputPanel 搭配下拉式方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690308"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a>使用 PenInputPanel 搭配下拉式方塊

\[[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件已由[>textinput](/previous-versions/ms581554(v=vs.100))取代。 請參閱 [文字輸入面板](programming-the-text-input-panel.md)的程式設計。\]

如果您將 [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) 物件附加至 [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) 控制項，則在執行時間時，請在 [編輯控制項部分] 下拉式方塊上，按下 tablet 畫筆，PenInputPanel 物件就不會出現。 但是，如果您點擊下拉箭號，就會出現此情況。 這是因為下拉式方塊中編輯控制項的視窗不是接收畫筆訊息的視窗。 下拉式方塊具有子編輯視窗。 這個問題的解決方法是判斷 PenInputPanel 物件是否附加的視窗具有子視窗。 若是如此，您可以將 PenInputPanel 物件附加至子視窗。

將[PenInputPanel](/previous-versions/aa514041(v=msdn.10))物件的[system.windows.controls.primitives.popup.verticaloffset](/previous-versions/ms571983(v=vs.100))屬性設定為-1 時，面板會顯示在下拉式方塊的上方。

 

 
