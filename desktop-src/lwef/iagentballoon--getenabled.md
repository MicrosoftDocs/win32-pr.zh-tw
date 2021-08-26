---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d144374f690d295b80d0092add56439eb4e5fc9d546ba1f970ab99976cf2d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888389"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon：： GetEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

抓取文字氣球的 [**Enabled**](enabled-property.md) 屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

在啟用文字批註時接收 **True** 的變數位址，以及停用時的 **False** 。

</dd> </dl>

除非已停用，否則 Microsoft 代理程式伺服器會自動顯示語音輸出的文字提示。 您可以針對 Microsoft Agent 字元編輯器中的字元停用文字批註，或由使用者)  (Microsoft Agent 屬性工作表中的所有字元。 如果使用者停用文字提示，用戶端就無法將它還原。

 

 




