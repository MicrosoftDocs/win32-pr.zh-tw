---
description: LoadXML 方法會載入可延伸標記語言 (XML)  (XML) 中表示的屬性資料。
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'IPropertySetter：： LoadXML 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991562"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="fe132-103">IPropertySetter：： LoadXML 方法</span><span class="sxs-lookup"><span data-stu-id="fe132-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="fe132-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fe132-104">\[Deprecated.</span></span> <span data-ttu-id="fe132-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fe132-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe132-106">`LoadXML`方法會載入以可延伸標記語言 (XML)  (XML) 表示的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="fe132-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe132-107">語法</span><span class="sxs-lookup"><span data-stu-id="fe132-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="fe132-108">參數</span><span class="sxs-lookup"><span data-stu-id="fe132-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe132-109">*.pxml* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe132-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe132-110">Microsoft XML 剖析器所建立之 XML 元素的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fe132-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe132-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe132-111">Return value</span></span>

<span data-ttu-id="fe132-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fe132-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fe132-113">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="fe132-113">Possible values include the following.</span></span>



| <span data-ttu-id="fe132-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fe132-114">Return code</span></span>                                                                                                  | <span data-ttu-id="fe132-115">Description</span><span class="sxs-lookup"><span data-stu-id="fe132-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="fe132-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="fe132-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="fe132-117">沒有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="fe132-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="fe132-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fe132-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="fe132-119">成功。</span><span class="sxs-lookup"><span data-stu-id="fe132-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="fe132-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fe132-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="fe132-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="fe132-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="fe132-122"><dt>**VFW \_ E \_ 不正確 \_ 檔 \_ 格式**</dt></span><span class="sxs-lookup"><span data-stu-id="fe132-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="fe132-123">格式無效。</span><span class="sxs-lookup"><span data-stu-id="fe132-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="fe132-124">備註</span><span class="sxs-lookup"><span data-stu-id="fe132-124">Remarks</span></span>

<span data-ttu-id="fe132-125">一般來說，應用程式不需要使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="fe132-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="fe132-126">DES 在內部使用它從 XTL 檔案載入屬性。</span><span class="sxs-lookup"><span data-stu-id="fe132-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="fe132-127">若要使用此方法，請建立 **IXMLDocument** 物件，並使用它來剖析 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="fe132-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="fe132-128">然後使用 **IXMLDocument** 物件來取出 **IXMLElement** 物件。</span><span class="sxs-lookup"><span data-stu-id="fe132-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="fe132-129">如果物件有屬性，您可以將 **IXMLElement** 指標傳遞給 **LoadXML** 方法。</span><span class="sxs-lookup"><span data-stu-id="fe132-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="fe132-130">方法會將屬性載入至屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="fe132-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="fe132-131">**IXMLDocument** 和 **IXMLElement** 介面是在 Microsoft XML Core Services (msxml) 1.0 版中執行，但不會在較新版本的 msxml 中執行。</span><span class="sxs-lookup"><span data-stu-id="fe132-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe132-132">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fe132-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe132-133">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fe132-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fe132-134">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fe132-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe132-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe132-135">Requirements</span></span>



| <span data-ttu-id="fe132-136">需求</span><span class="sxs-lookup"><span data-stu-id="fe132-136">Requirement</span></span> | <span data-ttu-id="fe132-137">值</span><span class="sxs-lookup"><span data-stu-id="fe132-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe132-138">標頭</span><span class="sxs-lookup"><span data-stu-id="fe132-138">Header</span></span><br/>  | <dl> <span data-ttu-id="fe132-139"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe132-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fe132-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe132-140">Library</span></span><br/> | <dl> <span data-ttu-id="fe132-141"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe132-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe132-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe132-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe132-143">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="fe132-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="fe132-144">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="fe132-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




