---
title: 通用控制項的當地語系化支援
description: 本主題說明通用控制項內建的國家語言的支援。
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932007"
---
# <a name="localization-support-for-common-controls"></a>通用控制項的當地語系化支援

本主題說明通用控制項內建的國家語言的支援。 內建的國家語言支援可簡化當地語系化應用程式的執行。

本主題包含下列幾節：

-   [指定通用控制項的語言](#specifying-a-language-for-the-common-controls)
-   [在對話方塊中指定控制項的語言](#specifying-a-language-for-controls-in-a-dialog-box)
-   [相關主題](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a>指定通用控制項的語言

如果您想要指定與系統語言不同之通用控制項的語言，請呼叫 [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)。 這個函式所指定的語言只會套用至呼叫函式的進程。

若要判斷通用控制項目前所使用的語言，請呼叫 [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage)。 它會傳回先前呼叫 [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)所設定的值。 傳回的語言是針對呼叫它的進程所指定的語言。 如果尚未呼叫 **InitMUILanguage** ，或從另一個進程呼叫， **GetMUILanguage** 將會傳回預設值。

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a>在對話方塊中指定控制項的語言

不同于通用控制項，預先定義的控制項（例如按鈕或編輯方塊）預設不會使用目前的系統語言。 原生字型控制項是不可見的控制項，可在背景中運作，以允許對話方塊的預先定義控制項顯示目前的系統語言。

若要使用原生字型控制項，請遵循此程式。

1.  藉由呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)來初始化原生字型控制項。 將 *lpInitCtrls* 所指向之 [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **DWICC** 成員設定為 [ICC \_ NATIVEFNTCTL \_ 類別]。
2.  將控制項新增至對話方塊的資源腳本。 設定下列一或多個樣式旗標，以指定將會影響哪些控制項。 

    | 旗標              | 適用於                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NFS \_ 編輯         | 編輯控制項                                                                                                                                                                                                                                                    |
    | NFS \_ 靜態       | 靜態控制項                                                                                                                                                                                                                                                  |
    | NFS \_ LISTCOMBO    | 清單、ComboBox、清單視圖和 ComboBoxEx 控制項                                                                                                                                                                                                               |
    | NFS \_ 按鈕       | 按鈕控制項                                                                                                                                                                                                                                                  |
    | NFS \_ 全部          | 所有控制項                                                                                                                                                                                                                                                     |
    | NFS \_ USEFONTASSOC | 東亞平臺。 控制項使用字型關聯功能，而不是切換至原生字型。 所有其他平臺會忽略它。 Windows Vista 的這項功能已被取代，comctl v6 則不支援。 基於舊版原因，這存在於 comctl v5 中。 |

    

     

下列範例說明如何將原生字型控制項新增至資源腳本。 它會讓對話方塊的編輯、列出和下拉式方塊控制項使用目前的系統語言來顯示文字。


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於通用控制項](common-controls-intro.md)
</dt> </dl>

 

 




