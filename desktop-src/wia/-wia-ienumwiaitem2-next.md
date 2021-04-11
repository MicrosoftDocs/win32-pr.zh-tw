---
description: 填滿 IWiaItem2 介面的指標陣列。
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2：： Next 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191579"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="f1add-103">IEnumWiaItem2：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="f1add-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="f1add-104">填滿 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="f1add-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1add-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1add-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="f1add-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1add-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1add-107">*cElt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1add-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1add-108">類型： **ULONG**</span><span class="sxs-lookup"><span data-stu-id="f1add-108">Type: **ULONG**</span></span>

<span data-ttu-id="f1add-109">指定 *ppIWiaItem2* 參數所指定之陣列中的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="f1add-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f1add-110">*ppIWiaItem2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1add-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1add-111">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f1add-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="f1add-112">接收 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="f1add-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="f1add-113">**IEnumWiaItem2：： Next** 會使用介面指標填滿此陣列。</span><span class="sxs-lookup"><span data-stu-id="f1add-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="f1add-114">*pcEltFetched* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f1add-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1add-115">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="f1add-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="f1add-116">在輸出中，此參數會接收實際儲存在 _ppIWiaItem2 \* 參數所指出的陣列中的介面指標數目。</span><span class="sxs-lookup"><span data-stu-id="f1add-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="f1add-117">列舉完成時，此參數會包含零。</span><span class="sxs-lookup"><span data-stu-id="f1add-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1add-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1add-118">Return value</span></span>

<span data-ttu-id="f1add-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f1add-119">Type: **HRESULT**</span></span>

<span data-ttu-id="f1add-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f1add-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1add-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f1add-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1add-122">備註</span><span class="sxs-lookup"><span data-stu-id="f1add-122">Remarks</span></span>

<span data-ttu-id="f1add-123">Windows 映像取得 (WIA) 2.0 執行時間系統會將 WIA 2.0 硬體裝置表示為 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="f1add-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="f1add-124">應用程式會使用 **IEnumWiaItem2：： Next** 方法，為硬體裝置的 **IWiaItem2** 物件樹狀結構的目前資料夾中的每個專案取得 **IWiaItem2** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f1add-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="f1add-125">為了取得指標清單，應用程式會傳遞所配置之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="f1add-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="f1add-126">它也會在參數 *cElt* 中傳遞陣列元素的數目。</span><span class="sxs-lookup"><span data-stu-id="f1add-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="f1add-127">**IEnumWiaItem2：： Next** 方法會使用 **IWiaItem2** 介面的指標來填滿陣列。</span><span class="sxs-lookup"><span data-stu-id="f1add-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="f1add-128">在列舉程式完成之前， **IEnumWiaItem2：： Next** 方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f1add-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="f1add-129">它會在每次執行時，將 *pcEltFetched* 的值設定為它插入陣列中的專案數目。</span><span class="sxs-lookup"><span data-stu-id="f1add-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="f1add-130">當 **IEnumWiaItem2：： Next** 完成列舉 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的程式時，它會傳回 \_ FALSE，並將 *pcEltFetched* 所指向的記憶體位置設定為零。</span><span class="sxs-lookup"><span data-stu-id="f1add-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="f1add-131">應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="f1add-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1add-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1add-132">Requirements</span></span>



| <span data-ttu-id="f1add-133">需求</span><span class="sxs-lookup"><span data-stu-id="f1add-133">Requirement</span></span> | <span data-ttu-id="f1add-134">值</span><span class="sxs-lookup"><span data-stu-id="f1add-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f1add-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1add-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f1add-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1add-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f1add-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1add-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f1add-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1add-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f1add-139">標頭</span><span class="sxs-lookup"><span data-stu-id="f1add-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1add-140"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="f1add-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1add-141">Idl</span><span class="sxs-lookup"><span data-stu-id="f1add-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1add-142"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1add-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
