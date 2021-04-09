---
description: 建立可開始交易的泛型交易式物件。 藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: 'TransactionCoNtextEx 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689096"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="a342e-104">TransactionCoNtextEx 類別</span><span class="sxs-lookup"><span data-stu-id="a342e-104">TransactionContextEx class</span></span>

<span data-ttu-id="a342e-105">建立可開始交易的泛型交易式物件。</span><span class="sxs-lookup"><span data-stu-id="a342e-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="a342e-106">藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="a342e-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a342e-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="a342e-107">When to implement</span></span>

<span data-ttu-id="a342e-108">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="a342e-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="a342e-109">需求</span><span class="sxs-lookup"><span data-stu-id="a342e-109">Requirement</span></span> | <span data-ttu-id="a342e-110">值</span><span class="sxs-lookup"><span data-stu-id="a342e-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="a342e-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="a342e-111">CLSID</span></span>      | <span data-ttu-id="a342e-112">CLSID \_ TransactionCoNtextEx</span><span class="sxs-lookup"><span data-stu-id="a342e-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="a342e-113">ProgID</span><span class="sxs-lookup"><span data-stu-id="a342e-113">ProgID</span></span>     | <span data-ttu-id="a342e-114">L "TxCTx. TransactionCoNtextEx"</span><span class="sxs-lookup"><span data-stu-id="a342e-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="a342e-115">介面</span><span class="sxs-lookup"><span data-stu-id="a342e-115">Interfaces</span></span> | [<span data-ttu-id="a342e-116">**ITransactionCoNtextEx**</span><span class="sxs-lookup"><span data-stu-id="a342e-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="a342e-117">使用時機</span><span class="sxs-lookup"><span data-stu-id="a342e-117">When to use</span></span>

<span data-ttu-id="a342e-118">非交易式用戶端會使用這個類別來開始交易。</span><span class="sxs-lookup"><span data-stu-id="a342e-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="a342e-119">使用這個類別的方法，用戶端可以呼叫在交易內容物件的交易界限內執行的其他 COM 物件（如果已設定為參與交易）。</span><span class="sxs-lookup"><span data-stu-id="a342e-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="a342e-120">根據其商務邏輯，用戶端可以明確地認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="a342e-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="a342e-121">**TransactionCoNtextEx** 類別限制重複使用推動交易的商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="a342e-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="a342e-122">基於這個理由，建議您不要使用 **TransactionCoNtextEx** 類別所具現化的物件。</span><span class="sxs-lookup"><span data-stu-id="a342e-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="a342e-123">備註</span><span class="sxs-lookup"><span data-stu-id="a342e-123">Remarks</span></span>

<span data-ttu-id="a342e-124">若要建立這個物件，請呼叫 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)。</span><span class="sxs-lookup"><span data-stu-id="a342e-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="a342e-125">**TransactionCoNtextEx** 類別並非設計用來 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="a342e-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="a342e-126">請改用 [**TransactionCoNtext**](transactioncontext.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="a342e-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="a342e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a342e-127">Requirements</span></span>



| <span data-ttu-id="a342e-128">需求</span><span class="sxs-lookup"><span data-stu-id="a342e-128">Requirement</span></span> | <span data-ttu-id="a342e-129">值</span><span class="sxs-lookup"><span data-stu-id="a342e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a342e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a342e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a342e-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a342e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a342e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a342e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a342e-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a342e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a342e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="a342e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a342e-135"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="a342e-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a342e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a342e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a342e-137">設定交易</span><span class="sxs-lookup"><span data-stu-id="a342e-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="a342e-138">**ITransactionCoNtextEx**</span><span class="sxs-lookup"><span data-stu-id="a342e-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="a342e-139">**TransactionCoNtext**</span><span class="sxs-lookup"><span data-stu-id="a342e-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 




