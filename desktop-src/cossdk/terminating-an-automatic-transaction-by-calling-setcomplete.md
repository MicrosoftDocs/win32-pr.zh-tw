---
description: 藉由呼叫 SetComplete 來終止自動交易
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: 藉由呼叫 SetComplete 來終止自動交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972770"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>藉由呼叫 SetComplete 來終止自動交易

若要有效地使用自動交易，每個交易元件都應該指出它已完成其工作。 當物件實例順利完成其工作時，會呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 方法（透過 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 介面和 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) 物件公開），將其一致且完成的旗標設定為 True。

完成自動交易最有效率的方式，就是使用 [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 方法來明確停用根物件。 藉由明確指出根物件已完成其工作，您可以減少交易的長度。

下列 Visual Basic 範例顯示如何表示交易對象已順利完成其工作：


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[一致且完成的旗標](consistent-and-done-flags.md)
</dt> <dt>

[管理 COM + 中的自動交易](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



