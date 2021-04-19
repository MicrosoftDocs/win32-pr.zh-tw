---
description: GetVendorString 方法會抓取廠商的名稱。 針對 DirectShow 所提供的轉譯引擎物件，廠商字串為 &\# 0034;Microsoft Corporation&\# 0034;。
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'IRenderEngine：： GetVendorString 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976174"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="2dc95-104">IRenderEngine：： GetVendorString 方法</span><span class="sxs-lookup"><span data-stu-id="2dc95-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="2dc95-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2dc95-105">\[Deprecated.</span></span> <span data-ttu-id="2dc95-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2dc95-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2dc95-107">方法會抓取 `GetVendorString` 廠商的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dc95-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="2dc95-108">針對 DirectShow 所提供的轉譯引擎物件，廠商字串為 "Microsoft Corporation"。</span><span class="sxs-lookup"><span data-stu-id="2dc95-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc95-109">語法</span><span class="sxs-lookup"><span data-stu-id="2dc95-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="2dc95-110">參數</span><span class="sxs-lookup"><span data-stu-id="2dc95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc95-111">*pVendorID* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="2dc95-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc95-112">接收包含廠商字串的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="2dc95-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc95-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dc95-113">Return value</span></span>

<span data-ttu-id="2dc95-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2dc95-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2dc95-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2dc95-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dc95-116">備註</span><span class="sxs-lookup"><span data-stu-id="2dc95-116">Remarks</span></span>

<span data-ttu-id="2dc95-117">方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="2dc95-117">The method allocates memory for the string.</span></span> <span data-ttu-id="2dc95-118">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="2dc95-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="2dc95-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2dc95-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2dc95-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2dc95-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2dc95-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2dc95-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2dc95-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dc95-122">Requirements</span></span>



| <span data-ttu-id="2dc95-123">需求</span><span class="sxs-lookup"><span data-stu-id="2dc95-123">Requirement</span></span> | <span data-ttu-id="2dc95-124">值</span><span class="sxs-lookup"><span data-stu-id="2dc95-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc95-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2dc95-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2dc95-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc95-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2dc95-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2dc95-127">Library</span></span><br/> | <dl> <span data-ttu-id="2dc95-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dc95-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc95-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dc95-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc95-130">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="2dc95-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="2dc95-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2dc95-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




