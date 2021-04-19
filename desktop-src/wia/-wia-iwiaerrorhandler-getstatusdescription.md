---
description: 傳回描述狀態碼的字串。
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'IWiaErrorHandler：： GetStatusDescription 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981436"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="c4c03-103">IWiaErrorHandler：： GetStatusDescription 方法</span><span class="sxs-lookup"><span data-stu-id="c4c03-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="c4c03-104">傳回描述狀態碼的字串。</span><span class="sxs-lookup"><span data-stu-id="c4c03-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c03-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4c03-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="c4c03-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4c03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c03-107">*punkItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c03-108">類型： \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="c4c03-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="c4c03-109">正在傳送之專案的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。</span><span class="sxs-lookup"><span data-stu-id="c4c03-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="c4c03-110">此物件至少會執行 [_ *IWiaItem2* \*](-wia-iwiaitem2.md)和 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)。</span><span class="sxs-lookup"><span data-stu-id="c4c03-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="c4c03-111">*hrStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c03-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4c03-112">Type: **HRESULT**</span></span>

<span data-ttu-id="c4c03-113">**HRESULT** ，這是 [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c4c03-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="c4c03-114">*cbResLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c03-115">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="c4c03-115">Type: **LONG**</span></span>

<span data-ttu-id="c4c03-116">**LONG** 是 *>pbdata* 所參考的資料大小。</span><span class="sxs-lookup"><span data-stu-id="c4c03-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="c4c03-117">*>pbdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c03-118">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="c4c03-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="c4c03-119">[_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)所接收之資料緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="c4c03-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="c4c03-120">*pbstrDescription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4c03-121">類型： \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="c4c03-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="c4c03-122">_ *BSTR*\* 接收資料傳輸期間發生之狀態或錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="c4c03-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="c4c03-123">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c4c03-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="c4c03-124">呼叫端必須使用 [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)釋放字串，而實作項必須使用 [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)來配置字串。</span><span class="sxs-lookup"><span data-stu-id="c4c03-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c03-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4c03-125">Return value</span></span>

<span data-ttu-id="c4c03-126">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4c03-126">Type: **HRESULT**</span></span>

<span data-ttu-id="c4c03-127">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c4c03-127">Returns one of the following values.</span></span>



| <span data-ttu-id="c4c03-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c4c03-128">Return code</span></span>                                                                             | <span data-ttu-id="c4c03-129">Description</span><span class="sxs-lookup"><span data-stu-id="c4c03-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4c03-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c03-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c4c03-131">*pbstrDescription* 包含有效的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="c4c03-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="c4c03-132"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c03-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c4c03-133">*hrStatus* 未知，而且沒有可用的描述。</span><span class="sxs-lookup"><span data-stu-id="c4c03-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="c4c03-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4c03-134">Requirements</span></span>



| <span data-ttu-id="c4c03-135">需求</span><span class="sxs-lookup"><span data-stu-id="c4c03-135">Requirement</span></span> | <span data-ttu-id="c4c03-136">值</span><span class="sxs-lookup"><span data-stu-id="c4c03-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c03-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4c03-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c03-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c4c03-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4c03-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c03-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4c03-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4c03-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c4c03-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c03-142"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="c4c03-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="c4c03-143">Idl</span><span class="sxs-lookup"><span data-stu-id="c4c03-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4c03-144"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4c03-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="c4c03-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4c03-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4c03-146"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4c03-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
