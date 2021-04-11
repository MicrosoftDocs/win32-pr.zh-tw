---
description: 建立可開始交易的泛型交易式物件。
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: 'TransactionCoNtext 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191004"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="f8b01-103">TransactionCoNtext 類別</span><span class="sxs-lookup"><span data-stu-id="f8b01-103">TransactionContext class</span></span>

<span data-ttu-id="f8b01-104">建立可開始交易的泛型交易式物件。</span><span class="sxs-lookup"><span data-stu-id="f8b01-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="f8b01-105">藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="f8b01-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f8b01-106">執行時機</span><span class="sxs-lookup"><span data-stu-id="f8b01-106">When to implement</span></span>

<span data-ttu-id="f8b01-107">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="f8b01-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f8b01-108">需求</span><span class="sxs-lookup"><span data-stu-id="f8b01-108">Requirement</span></span> | <span data-ttu-id="f8b01-109">值</span><span class="sxs-lookup"><span data-stu-id="f8b01-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="f8b01-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="f8b01-110">CLSID</span></span>      | <span data-ttu-id="f8b01-111">CLSID \_ TransactionCoNtext</span><span class="sxs-lookup"><span data-stu-id="f8b01-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="f8b01-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="f8b01-112">ProgID</span></span>     | <span data-ttu-id="f8b01-113">L "TxCTx. TransactionCoNtext"</span><span class="sxs-lookup"><span data-stu-id="f8b01-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="f8b01-114">介面</span><span class="sxs-lookup"><span data-stu-id="f8b01-114">Interfaces</span></span> | [<span data-ttu-id="f8b01-115">**ITransactionCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f8b01-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="f8b01-116">使用時機</span><span class="sxs-lookup"><span data-stu-id="f8b01-116">When to use</span></span>

<span data-ttu-id="f8b01-117">非交易式用戶端會使用這個類別來開始交易。</span><span class="sxs-lookup"><span data-stu-id="f8b01-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="f8b01-118">使用這個類別的方法，用戶端可以呼叫在交易內容物件的交易界限內執行的其他 COM 物件（如果已設定為參與交易）。</span><span class="sxs-lookup"><span data-stu-id="f8b01-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="f8b01-119">根據其商務邏輯，用戶端可以明確地認可或中止交易。</span><span class="sxs-lookup"><span data-stu-id="f8b01-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="f8b01-120">**TransactionCoNtext** 類別限制重複使用推動交易的商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="f8b01-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="f8b01-121">基於這個理由，建議您不要使用 **TransactionCoNtext** 類別所具現化的物件。</span><span class="sxs-lookup"><span data-stu-id="f8b01-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8b01-122">備註</span><span class="sxs-lookup"><span data-stu-id="f8b01-122">Remarks</span></span>

<span data-ttu-id="f8b01-123">若要建立這個物件，請呼叫 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)。</span><span class="sxs-lookup"><span data-stu-id="f8b01-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="f8b01-124">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="f8b01-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="f8b01-125">您可以使用 "COMSVCSLib. TransactionCoNtext" 將 TransactionCoNtext 物件宣告為類別名稱。</span><span class="sxs-lookup"><span data-stu-id="f8b01-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b01-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8b01-126">Requirements</span></span>



| <span data-ttu-id="f8b01-127">需求</span><span class="sxs-lookup"><span data-stu-id="f8b01-127">Requirement</span></span> | <span data-ttu-id="f8b01-128">值</span><span class="sxs-lookup"><span data-stu-id="f8b01-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b01-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8b01-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b01-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8b01-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8b01-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8b01-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b01-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8b01-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8b01-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f8b01-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b01-134"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b01-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b01-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8b01-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b01-136">設定交易</span><span class="sxs-lookup"><span data-stu-id="f8b01-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="f8b01-137">**ITransactionCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f8b01-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="f8b01-138">**TransactionCoNtextEx**</span><span class="sxs-lookup"><span data-stu-id="f8b01-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 




