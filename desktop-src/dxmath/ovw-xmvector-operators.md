---
description: 下列運算子是由 XMVECTOR 結構所公開。
ms.assetid: 16fc1276-7bed-4e6f-8af5-d871afa73b68
title: XMVECTOR 運算子
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0611be5e9737e2829bc06f9a3fade10db233cbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976800"
---
# <a name="xmvector-operators"></a><span data-ttu-id="dd206-103">XMVECTOR 運算子</span><span class="sxs-lookup"><span data-stu-id="dd206-103">XMVECTOR Operators</span></span>

<span data-ttu-id="dd206-104">下列運算子是由 [**XMVECTOR**](xmvector-data-type.md) 結構所公開。</span><span class="sxs-lookup"><span data-stu-id="dd206-104">The following operators are exposed by the [**XMVECTOR**](xmvector-data-type.md) structure.</span></span>

> [!Note]  
> <span data-ttu-id="dd206-105">此處所列的運算子僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="dd206-105">The operators listed here are only available under C++.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="dd206-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="dd206-106">In this section</span></span>



| <span data-ttu-id="dd206-107">方法</span><span class="sxs-lookup"><span data-stu-id="dd206-107">Methods</span></span>                                                    | <span data-ttu-id="dd206-108">描述</span><span class="sxs-lookup"><span data-stu-id="dd206-108">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd206-109">[**運算子 + =**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd206-109">[**operator +=**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span></span><br/>  | <span data-ttu-id="dd206-110">將浮點值加入至 `XMVECTOR` 實例，並傳回已更新之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="dd206-110">Adds a floating point value to an `XMVECTOR` instance, and returns a reference to the updated instance.</span></span> <br/>                         |
| <span data-ttu-id="dd206-111">[**operator-=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd206-111">[**operator -=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span></span><br/>    | <span data-ttu-id="dd206-112">從目前的實例減去浮點值，並傳回 `XMVECTOR` 更新的目前實例中的結果。</span><span class="sxs-lookup"><span data-stu-id="dd206-112">Subtracts a floating point value from the current instance of `XMVECTOR`, returning the result in the updated current instance.</span></span> <br/> |
| [<span data-ttu-id="dd206-113">\**運算子 \** _</span><span class="sxs-lookup"><span data-stu-id="dd206-113">\**operator \** _</span></span>](xmvector-operator-mul.md)<br/>    | <span data-ttu-id="dd206-114">乘法運算子</span><span class="sxs-lookup"><span data-stu-id="dd206-114">Multiplication operators</span></span><br/>                                                                                                         |
| [<span data-ttu-id="dd206-115">_ *運算子 \* =*\*</span><span class="sxs-lookup"><span data-stu-id="dd206-115">_ *operator \*=*\*</span></span>](xmvector-operator-muleq.md)<br/> | <span data-ttu-id="dd206-116">乘法指派運算子</span><span class="sxs-lookup"><span data-stu-id="dd206-116">Multiplication assignment operators</span></span><br/>                                                                                              |
| [<span data-ttu-id="dd206-117">**運算子**</span><span class="sxs-lookup"><span data-stu-id="dd206-117">**operator /**</span></span>](xmvector-operator-div.md)<br/>     | <span data-ttu-id="dd206-118">除法運算子。</span><span class="sxs-lookup"><span data-stu-id="dd206-118">Division operator.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="dd206-119">**operator/=**</span><span class="sxs-lookup"><span data-stu-id="dd206-119">**operator /=**</span></span>](xmvector-operator-diveq.md)<br/>  | <span data-ttu-id="dd206-120">除法指派運算子。</span><span class="sxs-lookup"><span data-stu-id="dd206-120">Division Assignment operator.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="dd206-121">**運算子**</span><span class="sxs-lookup"><span data-stu-id="dd206-121">**operator -**</span></span>](xmvector-operator--.md)<br/>       | <span data-ttu-id="dd206-122">減法和負運算子</span><span class="sxs-lookup"><span data-stu-id="dd206-122">Subtraction and negation operators</span></span><br/>                                                                                               |
| [<span data-ttu-id="dd206-123">**運算子 +**</span><span class="sxs-lookup"><span data-stu-id="dd206-123">**operator +**</span></span>](xmvector-operator-pls.md)<br/>     | <span data-ttu-id="dd206-124">加法運算子。</span><span class="sxs-lookup"><span data-stu-id="dd206-124">Addition operators.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="dd206-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd206-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd206-126">XMVECTOR 延伸模組</span><span class="sxs-lookup"><span data-stu-id="dd206-126">XMVECTOR Extensions</span></span>](ovw-xmvector-extensions.md)
</dt> <dt>

<span data-ttu-id="dd206-127">**類型**</span><span class="sxs-lookup"><span data-stu-id="dd206-127">**Types**</span></span>
</dt> <dt>

[<span data-ttu-id="dd206-128">**XMVECTOR 資料類型**</span><span class="sxs-lookup"><span data-stu-id="dd206-128">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
