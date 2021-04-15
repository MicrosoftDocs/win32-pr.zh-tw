---
description: 使用物件的函式字串來建立元件
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: 使用物件的函式字串來建立元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468292"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>使用物件的函式字串來建立元件

下列範例說明如何在元件具現化時，以程式設計方式取得和使用物件的函式字串。 它會顯示 [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) 介面的執行，以抓取物件的函式字串。 然後可以剖析字串以設定初始值，或影響元件的行為。

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件的函數位符串概念](com--object-constructor-strings-concepts.md)
</dt> <dt>

[指定元件的物件表示函式字串](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



