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
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="dc271-103">藉由呼叫 SetComplete 來終止自動交易</span><span class="sxs-lookup"><span data-stu-id="dc271-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="dc271-104">若要有效地使用自動交易，每個交易元件都應該指出它已完成其工作。</span><span class="sxs-lookup"><span data-stu-id="dc271-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="dc271-105">當物件實例順利完成其工作時，會呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 方法（透過 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 介面和 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) 物件公開），將其一致且完成的旗標設定為 True。</span><span class="sxs-lookup"><span data-stu-id="dc271-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="dc271-106">完成自動交易最有效率的方式，就是使用 [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 方法來明確停用根物件。</span><span class="sxs-lookup"><span data-stu-id="dc271-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="dc271-107">藉由明確指出根物件已完成其工作，您可以減少交易的長度。</span><span class="sxs-lookup"><span data-stu-id="dc271-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="dc271-108">下列 Visual Basic 範例顯示如何表示交易對象已順利完成其工作：</span><span class="sxs-lookup"><span data-stu-id="dc271-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="dc271-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="dc271-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc271-110">一致且完成的旗標</span><span class="sxs-lookup"><span data-stu-id="dc271-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="dc271-111">管理 COM + 中的自動交易</span><span class="sxs-lookup"><span data-stu-id="dc271-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



