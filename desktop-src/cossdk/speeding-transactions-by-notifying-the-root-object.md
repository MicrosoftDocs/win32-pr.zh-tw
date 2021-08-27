---
description: 藉由通知根物件來加速交易
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: 藉由通知根物件來加速交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd84a041a43ef0aa4a9dc9d5dd034017925c2a42834eb383efcd256d962bd5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812562"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a>藉由通知根物件來加速交易

若要有效地使用自動交易，每個交易元件都應該指出它已完成其工作。 當物件實例順利完成其工作時，會呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 方法，將其一致和完成的旗標設定為 True。 當交易的所有內建物件都呼叫 **SetComplete** 時，您可以藉由呼叫其 **SetComplete** 方法來明確停用根物件，藉以終止交易。 藉由明確指出根物件已完成其工作，您可以減少交易的長度。

當交易對象方法失敗時，物件應該藉由呼叫 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 方法，將其一致旗標設為 False，並將其完成旗標設為 True。 藉由呼叫 **SetAbort** 方法，物件會將控制權傳回給它的呼叫者，並確保最終會中止交易。

不過，除非呼叫 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 的物件是交易的根，否則即使沒有任何專案可以儲存，也會繼續執行交易，而不會進行最後的中止。 若要加速終止失敗的交易，您可以引發錯誤，以警告根物件也呼叫 **SetAbort**。 完成時，根物件應該會將錯誤訊息傳送到其用戶端。

雖然您可以採取許多不同的方法來處理錯誤，但您的方法應該清楚地協調內建物件和根物件之間的通訊。

下列 Visual Basic 程式碼片段會顯示錯誤處理的一種方法。 在第一個片段中，內建物件會呼叫 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)、引發錯誤，並產生錯誤訊息，如下所示：

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

在第二個片段中，根物件會處理錯誤，並將訊息傳遞至其用戶端，如下所示：

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理 COM + 中的自動交易](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



