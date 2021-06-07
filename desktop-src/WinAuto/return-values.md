---
title: " (Windows 協助工具功能傳回值) "
description: 本主題說明最常見的傳回值，以及您可能較不常看到的其他傳回值。
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443989"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="4f0b1-103"> (Windows 協助工具功能傳回值) </span><span class="sxs-lookup"><span data-stu-id="4f0b1-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="4f0b1-104">本主題說明最常見的傳回值，以及您可能較不常看到的其他傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="4f0b1-105">一般傳回值</span><span class="sxs-lookup"><span data-stu-id="4f0b1-105">Common Return Values</span></span>

<span data-ttu-id="4f0b1-106">[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)方法會傳回下列其中一個值（定義于 winerror.h 中），或另一個標準元件物件模型 (COM) 錯誤碼：</span><span class="sxs-lookup"><span data-stu-id="4f0b1-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|   <span data-ttu-id="4f0b1-107">值</span><span class="sxs-lookup"><span data-stu-id="4f0b1-107">Value</span></span>                      |   <span data-ttu-id="4f0b1-108">描述</span><span class="sxs-lookup"><span data-stu-id="4f0b1-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0b1-109">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="4f0b1-109">S\_OK</span></span>                   | <span data-ttu-id="4f0b1-110">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-110">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="4f0b1-111">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="4f0b1-111">S\_FALSE</span></span>                | <span data-ttu-id="4f0b1-112">此方法已成功在部分中。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-112">The method succeeded in part.</span></span> <span data-ttu-id="4f0b1-113">當方法成功時，就會發生這種情況，但無法使用要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-113">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="4f0b1-114">例如， \_ 如果您呼叫 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 在指定的點上抓取子物件，而指定的點不在物件或物件的子系中，Microsoft Active Accessibility 會傳回 S FALSE。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-114">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="4f0b1-115">將 \_ 電子 \_ MEMBERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="4f0b1-115">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="4f0b1-116">物件不支援要求的屬性或動作。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-116">The object does not support the requested property or action.</span></span> <span data-ttu-id="4f0b1-117">例如，如果您要求 [值屬性](value-property.md)，則 push 按鈕會傳回這個值，因為它沒有值屬性。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-117">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="4f0b1-118">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="4f0b1-118">E\_NOTIMPL</span></span>              | <span data-ttu-id="4f0b1-119">此方法尚未實作。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-119">The method is not implemented.</span></span> <span data-ttu-id="4f0b1-120">當用戶端呼叫該作業系統尚未支援的方法時，就會出現這個值。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-120">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4f0b1-121">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4f0b1-121">E\_INVALIDARG</span></span>           | <span data-ttu-id="4f0b1-122">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-122">One or more arguments were not valid.</span></span> <span data-ttu-id="4f0b1-123">當呼叫端嘗試使用伺服器無法辨識的識別碼來識別子物件時，就會發生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-123">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="4f0b1-124">當用戶端嘗試識別沒有子系的物件內的子物件時，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-124">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="4f0b1-125">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="4f0b1-125">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="4f0b1-126">方法無法配置完成作業所需的記憶體，以順利完成作業。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-126">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="4f0b1-127">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="4f0b1-127">E\_FAIL</span></span>                 | <span data-ttu-id="4f0b1-128">發生不明或一般錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-128">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="4f0b1-129">其他傳回值</span><span class="sxs-lookup"><span data-stu-id="4f0b1-129">Additional Return Values</span></span>

<span data-ttu-id="4f0b1-130">以下是 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法可能會傳回的傳回值。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-130">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="4f0b1-131">這些傳回值和先前的值並不常見，但您應該注意它們。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-131">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|    <span data-ttu-id="4f0b1-132">值</span><span class="sxs-lookup"><span data-stu-id="4f0b1-132">Value</span></span>                    |    <span data-ttu-id="4f0b1-133">描述</span><span class="sxs-lookup"><span data-stu-id="4f0b1-133">Description</span></span>                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0b1-134">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="4f0b1-134">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="4f0b1-135">當您呼叫 get \_ accValue 來取得密碼控制項的值時，就會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="4f0b1-135">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="4f0b1-136">出現 \_ E \_ 例外狀況</span><span class="sxs-lookup"><span data-stu-id="4f0b1-136">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="4f0b1-137">共同 \_ 電子 \_ OBJNOTCONNECTED</span><span class="sxs-lookup"><span data-stu-id="4f0b1-137">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




