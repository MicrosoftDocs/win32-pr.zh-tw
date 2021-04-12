---
title: 裝置錯誤碼
description: InvokeAction 和 QueryStateVariable 方法會傳回 HRESULT 值，這些值可能指出裝置錯誤 (也就是從 UPnP 認證的裝置) 收到的錯誤。
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463857"
---
# <a name="device-error-codes"></a><span data-ttu-id="3b90a-103">裝置錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3b90a-103">Device Error Codes</span></span>

<span data-ttu-id="3b90a-104">[**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)和 [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)方法會傳回 **HRESULT** 值，這些值可能指出裝置錯誤 (也就是從 UPnP 認證的裝置) 收到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b90a-104">The [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods return **HRESULT** values that might indicate a device error (that is, an error that is received from a UPnP-certified device).</span></span> <span data-ttu-id="3b90a-105">如果從裝置收到錯誤，則 ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 或) [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) 的方法會傳回以裝置錯誤碼為基礎的 **HRESULT** 值，如本主題中所述。</span><span class="sxs-lookup"><span data-stu-id="3b90a-105">If an error is received from a device, the method ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) or [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) returns an **HRESULT** value that is based on the device error code, as explained in this topic.</span></span> <span data-ttu-id="3b90a-106">因為轉換會套用至裝置錯誤碼以產生 **HRESULT** 值，所以您無法直接從 **HRESULT** 值讀取裝置錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b90a-106">Because a conversion is applied to the device error code to produce an **HRESULT** value, you cannot read the device error code directly from the **HRESULT** value.</span></span>

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a><span data-ttu-id="3b90a-107">將裝置錯誤碼轉換成 HRESULT</span><span class="sxs-lookup"><span data-stu-id="3b90a-107">Conversion of a Device Error Code to an HRESULT</span></span>

<span data-ttu-id="3b90a-108">有標準和非標準裝置錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b90a-108">There are both standard and non-standard device error codes.</span></span> <span data-ttu-id="3b90a-109">標準程式碼在所有 UPnP 認證的裝置上具有相同的意義，而且其值小於600。</span><span class="sxs-lookup"><span data-stu-id="3b90a-109">The standard codes have the same meaning across all UPnP-certified devices and have values that are less than 600.</span></span> <span data-ttu-id="3b90a-110">非標準的代碼是廠商專屬的，其值範圍從600到899。</span><span class="sxs-lookup"><span data-stu-id="3b90a-110">The non-standard codes are vendor-specific and have values ranging from 600 through 899.</span></span>

<span data-ttu-id="3b90a-111">裝置錯誤碼是否為標準，會決定 **HRESULT** 值的產生方式：</span><span class="sxs-lookup"><span data-stu-id="3b90a-111">Whether or not the device error code is standard determines how the **HRESULT** value is generated:</span></span>

-   <span data-ttu-id="3b90a-112">標準裝置錯誤碼對應至 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3b90a-112">A standard device error code is mapped to an **HRESULT** value.</span></span>

<!-- -->

-   <span data-ttu-id="3b90a-113">非標準的裝置錯誤碼會藉由套用公式內嵌于 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3b90a-113">A non-standard device error code is embedded in the **HRESULT** value by applying a formula.</span></span>

<span data-ttu-id="3b90a-114">這兩個程式都可以反轉，以判斷來自特定 **HRESULT** 值的裝置錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b90a-114">Both of these procedures can be reversed to determine the device error code from a particular **HRESULT** value.</span></span>

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a><span data-ttu-id="3b90a-115">從 HRESULT 值衍生裝置錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3b90a-115">Deriving a Device Error Code from an HRESULT Value</span></span>

<span data-ttu-id="3b90a-116">如果 **HRESULT** 值大於或等於 **upnp \_ e \_ 動作 \_ 特定 \_ 基底** (0x80040300) 且小於或等於 **upnp \_ e \_ 動作 \_ 特定的 \_ 最大** (0x8004042B) ，則裝置錯誤碼並非標準用法，請使用下一節中的公式來判斷錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b90a-116">If the **HRESULT** value is greater than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_BASE** (0x80040300) and less than or equal to **UPNP\_E\_ACTION\_SPECIFIC\_MAX** (0x8004042B), the device error code is nonstandard — use the formula in the following section to determine the error code.</span></span> <span data-ttu-id="3b90a-117">否則，裝置錯誤碼是標準的-使用對應中的 [標準裝置錯誤碼] 區段的表格，提供從 **HRESULT** 值到裝置錯誤碼的對應。</span><span class="sxs-lookup"><span data-stu-id="3b90a-117">Otherwise, the device error code is standard — use the table in the Mapping for Standard Device Error Codes section, which provides the mapping from the **HRESULT** value to the device error code.</span></span>

<span data-ttu-id="3b90a-118">如需呼叫 [**IUPnPService：： InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)之後之錯誤的文字描述，請將 *pvarRetVal* 參數設定為空陣列。</span><span class="sxs-lookup"><span data-stu-id="3b90a-118">For a text description of the error after a call to [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), set the *pvarRetVal* parameter to an empty array.</span></span> <span data-ttu-id="3b90a-119">傳回時，如果發生錯誤，此參數將包含錯誤的文字描述。</span><span class="sxs-lookup"><span data-stu-id="3b90a-119">Upon return, this parameter will contain a text description of the error, if any occurred.</span></span>

### <a name="formula-for-nonstandard-device-error-codes"></a><span data-ttu-id="3b90a-120">非標準裝置錯誤碼的公式</span><span class="sxs-lookup"><span data-stu-id="3b90a-120">Formula for Nonstandard Device Error Codes</span></span>

<span data-ttu-id="3b90a-121">如果 **upnp \_ e \_ 動作 \_ 特定的 \_ 基底** ≤ **HRESULT** ≤**upnp \_ e \_ 動作特定的 \_ \_ 最大值**，請使用下列公式。</span><span class="sxs-lookup"><span data-stu-id="3b90a-121">Use the following formula if **UPNP\_E\_ACTION\_SPECIFIC\_BASE** ≤ **HRESULT** ≤**UPNP\_E\_ACTION\_SPECIFIC\_MAX**.</span></span>

<span data-ttu-id="3b90a-122">裝置錯誤碼 = (**HRESULT**  -  **UPNP \_ E \_ 動作特定的 \_ \_ 基底**) +**錯誤 \_ 動作特定的 \_ \_ 基底**</span><span class="sxs-lookup"><span data-stu-id="3b90a-122">Device Error Code = (**HRESULT** - **UPNP\_E\_ACTION\_SPECIFIC\_BASE**) + **FAULT\_ACTION\_SPECIFIC\_BASE**</span></span>

<span data-ttu-id="3b90a-123">替代實際數值，方程式是：裝置錯誤碼 = (**HRESULT** -0x80040300) + 0x0258</span><span class="sxs-lookup"><span data-stu-id="3b90a-123">Substituting the actual numeric values, the equation is: Device Error Code = (**HRESULT** - 0x80040300) + 0x0258</span></span>

### <a name="mapping-for-standard-device-error-codes"></a><span data-ttu-id="3b90a-124">標準裝置的對應錯誤代碼</span><span class="sxs-lookup"><span data-stu-id="3b90a-124">Mapping for Standard Device Error Codes</span></span>

<span data-ttu-id="3b90a-125">如果 **HRESULT**  <  **UPNP \_ E \_ 動作 \_ 特定的 \_ 基底**，請使用下列對應。</span><span class="sxs-lookup"><span data-stu-id="3b90a-125">Use the following mapping if **HRESULT** < **UPNP\_E\_ACTION\_SPECIFIC\_BASE**.</span></span>



| <span data-ttu-id="3b90a-126">HRESULT 值</span><span class="sxs-lookup"><span data-stu-id="3b90a-126">HRESULT value</span></span>                    | <span data-ttu-id="3b90a-127">裝置錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3b90a-127">Device Error Code</span></span>                | <span data-ttu-id="3b90a-128">實際值</span><span class="sxs-lookup"><span data-stu-id="3b90a-128">Actual value</span></span> |
|----------------------------------|----------------------------------|--------------|
| <span data-ttu-id="3b90a-129">UPNP \_ E \_ 不正確 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="3b90a-129">UPNP\_E\_INVALID\_ACTION</span></span>         | <span data-ttu-id="3b90a-130">錯誤 \_ 不正確 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="3b90a-130">FAULT\_INVALID\_ACTION</span></span>           | <span data-ttu-id="3b90a-131">401</span><span class="sxs-lookup"><span data-stu-id="3b90a-131">401</span></span>          |
| <span data-ttu-id="3b90a-132">UPNP \_ E \_ 不正確 \_ 引數</span><span class="sxs-lookup"><span data-stu-id="3b90a-132">UPNP\_E\_INVALID\_ARGUMENTS</span></span>      | <span data-ttu-id="3b90a-133">錯誤 \_ 不正確 \_ ARG</span><span class="sxs-lookup"><span data-stu-id="3b90a-133">FAULT\_INVALID\_ARG</span></span>              | <span data-ttu-id="3b90a-134">402</span><span class="sxs-lookup"><span data-stu-id="3b90a-134">402</span></span>          |
| <span data-ttu-id="3b90a-135">UPNP \_ E \_ 不 \_ \_ 同步</span><span class="sxs-lookup"><span data-stu-id="3b90a-135">UPNP\_E\_OUT\_OF\_SYNC</span></span>           | <span data-ttu-id="3b90a-136">錯誤 \_ 不正確 \_ 序號 \_</span><span class="sxs-lookup"><span data-stu-id="3b90a-136">FAULT\_INVALID\_SEQUENCE\_NUMBER</span></span> | <span data-ttu-id="3b90a-137">403</span><span class="sxs-lookup"><span data-stu-id="3b90a-137">403</span></span>          |
| <span data-ttu-id="3b90a-138">UPNP \_ E \_ 不正確 \_ 變數</span><span class="sxs-lookup"><span data-stu-id="3b90a-138">UPNP\_E\_INVALID\_VARIABLE</span></span>       | <span data-ttu-id="3b90a-139">錯誤 \_ 不正確 \_ 變數</span><span class="sxs-lookup"><span data-stu-id="3b90a-139">FAULT\_INVALID\_VARIABLE</span></span>         | <span data-ttu-id="3b90a-140">404</span><span class="sxs-lookup"><span data-stu-id="3b90a-140">404</span></span>          |
| <span data-ttu-id="3b90a-141">UPNP \_ 電子 \_ 動作 \_ 要求 \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="3b90a-141">UPNP\_E\_ACTION\_REQUEST\_FAILED</span></span> | <span data-ttu-id="3b90a-142">錯誤 \_ 裝置 \_ 內部 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="3b90a-142">FAULT\_DEVICE\_INTERNAL\_ERROR</span></span>   | <span data-ttu-id="3b90a-143">501</span><span class="sxs-lookup"><span data-stu-id="3b90a-143">501</span></span>          |



 

## <a name="more-information"></a><span data-ttu-id="3b90a-144">相關資訊</span><span class="sxs-lookup"><span data-stu-id="3b90a-144">More Information</span></span>

<span data-ttu-id="3b90a-145">[UPnP 裝置架構版本 1.0](https://openconnectivity.org/resources/documents.asp)中指定了裝置錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b90a-145">Device error codes are specified in [UPnP Device Architecture version 1.0](https://openconnectivity.org/resources/documents.asp).</span></span> <span data-ttu-id="3b90a-146">本主題所述的常數定義于檔案的 Upnp 和 Upnp 中。</span><span class="sxs-lookup"><span data-stu-id="3b90a-146">The constants mentioned in this topic are defined in the files Upnp.h and Upnp.idl.</span></span>

 

 




