---
description: PrintXML 方法會將屬性資料轉換成 XML 字串。
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: 'IPropertySetter：:P rintXML 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977780"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="3972a-103">IPropertySetter：:P rintXML 方法</span><span class="sxs-lookup"><span data-stu-id="3972a-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="3972a-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3972a-104">\[Deprecated.</span></span> <span data-ttu-id="3972a-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3972a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3972a-106">`PrintXML`方法會將屬性資料轉換成 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="3972a-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3972a-107">語法</span><span class="sxs-lookup"><span data-stu-id="3972a-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="3972a-108">參數</span><span class="sxs-lookup"><span data-stu-id="3972a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3972a-109">*pszXML* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3972a-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3972a-110">接收 XML 字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="3972a-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="3972a-111">*cbXML* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3972a-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3972a-112">*PszXML* 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3972a-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3972a-113">*pcbPrinted* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3972a-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3972a-114">接收 XML 字串長度之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="3972a-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="3972a-115">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3972a-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3972a-116">*縮排* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3972a-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3972a-117">最外層標記的縮排層級數目。</span><span class="sxs-lookup"><span data-stu-id="3972a-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3972a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="3972a-118">Return value</span></span>

<span data-ttu-id="3972a-119">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="3972a-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="3972a-120">否則，會傳回 **HRESULT** 值，指出錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="3972a-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="3972a-121">如果 XML 字串的長度超過緩衝區，則方法會傳回 E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3972a-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3972a-122">備註</span><span class="sxs-lookup"><span data-stu-id="3972a-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3972a-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3972a-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3972a-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3972a-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3972a-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3972a-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3972a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3972a-126">Requirements</span></span>



| <span data-ttu-id="3972a-127">需求</span><span class="sxs-lookup"><span data-stu-id="3972a-127">Requirement</span></span> | <span data-ttu-id="3972a-128">值</span><span class="sxs-lookup"><span data-stu-id="3972a-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3972a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3972a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3972a-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3972a-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3972a-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3972a-131">Library</span></span><br/> | <dl> <span data-ttu-id="3972a-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3972a-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3972a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3972a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3972a-134">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="3972a-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="3972a-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3972a-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




