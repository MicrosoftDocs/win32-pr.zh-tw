---
description: 您可以使用 [元件服務] 系統管理工具手動設定交易屬性，也可以在撰寫元件時加入程式設計的交易支援。
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: 設定交易屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111277"
---
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="5c9ef-103">設定交易屬性</span><span class="sxs-lookup"><span data-stu-id="5c9ef-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="5c9ef-104">您可以使用 [元件服務] 系統管理工具手動設定交易屬性，也可以在撰寫元件時加入程式設計的交易支援。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="5c9ef-105">如需交易屬性值的詳細資訊，請參閱設定 [交易](configuring-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="5c9ef-106">**使用元件服務系統管理工具來設定屬性值**</span><span class="sxs-lookup"><span data-stu-id="5c9ef-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="5c9ef-107">在主控台樹中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="5c9ef-108">在 [元件屬性] 對話方塊中，按一下 [ **交易** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="5c9ef-109">在 [ **交易支援**] 下，選取您要的值選項。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="5c9ef-110">**不支援** 所有元件的預設值。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="5c9ef-111">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-111">Click **OK**.</span></span>

<span data-ttu-id="5c9ef-112">您必須為每個元件重複此程式。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="5c9ef-113">以程式設計方式設定屬性值</span><span class="sxs-lookup"><span data-stu-id="5c9ef-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="5c9ef-114">使用 Microsoft Visual Basic 的程式設計人員可以使用 **MTSTransactionMode**（ActiveX DLL 專案的類別模組屬性）設定 transaction 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="5c9ef-115">Visual Basic 將您的選取專案對應至相等的 COM + 交易屬性值，並在元件的類型程式庫中發佈此值。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="5c9ef-116">下表會將每個 **MTSTransactionMode** 常數值對應至其相等的 com + 交易值。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="5c9ef-117">MTSTransactionMode 常數</span><span class="sxs-lookup"><span data-stu-id="5c9ef-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="5c9ef-118">COM + 交易值</span><span class="sxs-lookup"><span data-stu-id="5c9ef-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="5c9ef-119">NotAnMTSObject (預設) </span><span class="sxs-lookup"><span data-stu-id="5c9ef-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="5c9ef-120">Disabled</span><span class="sxs-lookup"><span data-stu-id="5c9ef-120">Disabled</span></span><br/>                |
| <span data-ttu-id="5c9ef-121">NoTransactions</span><span class="sxs-lookup"><span data-stu-id="5c9ef-121">NoTransactions</span></span><br/>           | <span data-ttu-id="5c9ef-122"> (預設) 不支援</span><span class="sxs-lookup"><span data-stu-id="5c9ef-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="5c9ef-123">RequiresTransaction</span><span class="sxs-lookup"><span data-stu-id="5c9ef-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="5c9ef-124">必要</span><span class="sxs-lookup"><span data-stu-id="5c9ef-124">Required</span></span><br/>                |
| <span data-ttu-id="5c9ef-125">UsesTransaction</span><span class="sxs-lookup"><span data-stu-id="5c9ef-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="5c9ef-126">支援</span><span class="sxs-lookup"><span data-stu-id="5c9ef-126">Supported</span></span><br/>               |
| <span data-ttu-id="5c9ef-127">RequiresNewTransaction</span><span class="sxs-lookup"><span data-stu-id="5c9ef-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="5c9ef-128">必須是新交易</span><span class="sxs-lookup"><span data-stu-id="5c9ef-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="5c9ef-129">您也可以使用 COM + 系統管理程式庫 API，以程式設計方式存取 **MTSTransactionMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c9ef-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




