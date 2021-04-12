---
title: " (Windows 協助工具功能傳回值) "
description: 本主題說明最常見的傳回值，以及您可能較不常看到的其他傳回值。
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464012"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="afd05-103"> (Windows 協助工具功能傳回值) </span><span class="sxs-lookup"><span data-stu-id="afd05-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="afd05-104">本主題說明最常見的傳回值，以及您可能較不常看到的其他傳回值。</span><span class="sxs-lookup"><span data-stu-id="afd05-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="afd05-105">一般傳回值</span><span class="sxs-lookup"><span data-stu-id="afd05-105">Common Return Values</span></span>

<span data-ttu-id="afd05-106">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)方法會傳回下列其中一個值（定義于 winerror.h 中），或另一個標準元件物件模型 (COM) 錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="afd05-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afd05-107">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="afd05-107">S\_OK</span></span>                   | <span data-ttu-id="afd05-108">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="afd05-108">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="afd05-109">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="afd05-109">S\_FALSE</span></span>                | <span data-ttu-id="afd05-110">此方法已成功在部分中。</span><span class="sxs-lookup"><span data-stu-id="afd05-110">The method succeeded in part.</span></span> <span data-ttu-id="afd05-111">當方法成功時，就會發生這種情況，但無法使用要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="afd05-111">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="afd05-112">例如， \_ 如果您呼叫 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 在指定的點上抓取子物件，而指定的點不在物件或物件的子系中，Microsoft Active Accessibility 會傳回 S FALSE。</span><span class="sxs-lookup"><span data-stu-id="afd05-112">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="afd05-113">將 \_ 電子 \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="afd05-113">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="afd05-114">物件不支援要求的屬性或動作。</span><span class="sxs-lookup"><span data-stu-id="afd05-114">The object does not support the requested property or action.</span></span> <span data-ttu-id="afd05-115">例如，如果您要求 [值屬性](value-property.md)，則 push 按鈕會傳回這個值，因為它沒有值屬性。</span><span class="sxs-lookup"><span data-stu-id="afd05-115">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="afd05-116">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="afd05-116">E\_NOTIMPL</span></span>              | <span data-ttu-id="afd05-117">此方法尚未實作。</span><span class="sxs-lookup"><span data-stu-id="afd05-117">The method is not implemented.</span></span> <span data-ttu-id="afd05-118">當用戶端呼叫該作業系統尚未支援的方法時，就會出現這個值。</span><span class="sxs-lookup"><span data-stu-id="afd05-118">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="afd05-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="afd05-119">E\_INVALIDARG</span></span>           | <span data-ttu-id="afd05-120">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="afd05-120">One or more arguments were not valid.</span></span> <span data-ttu-id="afd05-121">當呼叫端嘗試使用伺服器無法辨識的識別碼來識別子物件時，就會發生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="afd05-121">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="afd05-122">當用戶端嘗試識別沒有子系的物件內的子物件時，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="afd05-122">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="afd05-123">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="afd05-123">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="afd05-124">方法無法配置完成作業所需的記憶體，以順利完成作業。</span><span class="sxs-lookup"><span data-stu-id="afd05-124">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="afd05-125">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="afd05-125">E\_FAIL</span></span>                 | <span data-ttu-id="afd05-126">發生不明或一般錯誤。</span><span class="sxs-lookup"><span data-stu-id="afd05-126">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="afd05-127">其他傳回值</span><span class="sxs-lookup"><span data-stu-id="afd05-127">Additional Return Values</span></span>

<span data-ttu-id="afd05-128">以下是 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法可能會傳回的傳回值。</span><span class="sxs-lookup"><span data-stu-id="afd05-128">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="afd05-129">這些傳回值和先前的值並不常見，但您應該注意它們。</span><span class="sxs-lookup"><span data-stu-id="afd05-129">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="afd05-130">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="afd05-130">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="afd05-131">當您呼叫 get \_ accValue 來取得密碼控制項的值時，就會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="afd05-131">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="afd05-132">出現 \_ E \_ 例外狀況</span><span class="sxs-lookup"><span data-stu-id="afd05-132">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="afd05-133">共同 \_ 電子 \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="afd05-133">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




