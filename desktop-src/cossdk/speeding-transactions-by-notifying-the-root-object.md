---
description: 藉由通知根物件來加速交易
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: 藉由通知根物件來加速交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187686"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="7103b-103">藉由通知根物件來加速交易</span><span class="sxs-lookup"><span data-stu-id="7103b-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="7103b-104">若要有效地使用自動交易，每個交易元件都應該指出它已完成其工作。</span><span class="sxs-lookup"><span data-stu-id="7103b-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="7103b-105">當物件實例順利完成其工作時，會呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 方法，將其一致和完成的旗標設定為 True。</span><span class="sxs-lookup"><span data-stu-id="7103b-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="7103b-106">當交易的所有內建物件都呼叫 **SetComplete** 時，您可以藉由呼叫其 **SetComplete** 方法來明確停用根物件，藉以終止交易。</span><span class="sxs-lookup"><span data-stu-id="7103b-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="7103b-107">藉由明確指出根物件已完成其工作，您可以減少交易的長度。</span><span class="sxs-lookup"><span data-stu-id="7103b-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="7103b-108">當交易對象方法失敗時，物件應該藉由呼叫 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 方法，將其一致旗標設為 False，並將其完成旗標設為 True。</span><span class="sxs-lookup"><span data-stu-id="7103b-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="7103b-109">藉由呼叫 **SetAbort** 方法，物件會將控制權傳回給它的呼叫者，並確保最終會中止交易。</span><span class="sxs-lookup"><span data-stu-id="7103b-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="7103b-110">不過，除非呼叫 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 的物件是交易的根，否則即使沒有任何專案可以儲存，也會繼續執行交易，而不會進行最後的中止。</span><span class="sxs-lookup"><span data-stu-id="7103b-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="7103b-111">若要加速終止失敗的交易，您可以引發錯誤，以警告根物件也呼叫 **SetAbort**。</span><span class="sxs-lookup"><span data-stu-id="7103b-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="7103b-112">完成時，根物件應該會將錯誤訊息傳送到其用戶端。</span><span class="sxs-lookup"><span data-stu-id="7103b-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="7103b-113">雖然您可以採取許多不同的方法來處理錯誤，但您的方法應該清楚地協調內建物件和根物件之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="7103b-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="7103b-114">下列 Visual Basic 程式碼片段會顯示錯誤處理的一種方法。</span><span class="sxs-lookup"><span data-stu-id="7103b-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="7103b-115">在第一個片段中，內建物件會呼叫 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)、引發錯誤，並產生錯誤訊息，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7103b-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="7103b-116">在第二個片段中，根物件會處理錯誤，並將訊息傳遞至其用戶端，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7103b-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="7103b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="7103b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7103b-118">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="7103b-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



