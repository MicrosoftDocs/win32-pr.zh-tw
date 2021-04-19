---
description: WriteXMLFile 方法會將時間軸轉譯成 XML，並將 XML 資料寫入檔案。
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex：： WriteXMLFile 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996276"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="d128b-103">IXml2Dex：： WriteXMLFile 方法</span><span class="sxs-lookup"><span data-stu-id="d128b-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="d128b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d128b-104">\[Deprecated.</span></span> <span data-ttu-id="d128b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d128b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d128b-106">方法會將 `WriteXMLFile` 時間軸轉譯成 xml，並將 xml 資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="d128b-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d128b-107">語法</span><span class="sxs-lookup"><span data-stu-id="d128b-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d128b-108">參數</span><span class="sxs-lookup"><span data-stu-id="d128b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d128b-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="d128b-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="d128b-110">時間軸物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="d128b-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="d128b-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d128b-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d128b-112">字串，指定要寫入的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d128b-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d128b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d128b-113">Return value</span></span>

<span data-ttu-id="d128b-114">傳回 **HRESULT** 值，此值相依于介面的執行。</span><span class="sxs-lookup"><span data-stu-id="d128b-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="d128b-115">**HRESULT** 可以包含下列其中一個標準常數，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="d128b-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="d128b-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d128b-116">Return code</span></span>                                                                                   | <span data-ttu-id="d128b-117">Description</span><span class="sxs-lookup"><span data-stu-id="d128b-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="d128b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d128b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d128b-119">引數無效。</span><span class="sxs-lookup"><span data-stu-id="d128b-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="d128b-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d128b-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d128b-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d128b-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="d128b-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d128b-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d128b-123">成功。</span><span class="sxs-lookup"><span data-stu-id="d128b-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d128b-124">備註</span><span class="sxs-lookup"><span data-stu-id="d128b-124">Remarks</span></span>

<span data-ttu-id="d128b-125">這個方法會產生 XML 檔案，代表時間軸中的所有元件。</span><span class="sxs-lookup"><span data-stu-id="d128b-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="d128b-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d128b-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d128b-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d128b-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d128b-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d128b-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d128b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d128b-129">Requirements</span></span>



| <span data-ttu-id="d128b-130">需求</span><span class="sxs-lookup"><span data-stu-id="d128b-130">Requirement</span></span> | <span data-ttu-id="d128b-131">值</span><span class="sxs-lookup"><span data-stu-id="d128b-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d128b-132">版本</span><span class="sxs-lookup"><span data-stu-id="d128b-132">Version</span></span><br/> | <span data-ttu-id="d128b-133">Internet Explorer 4.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d128b-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="d128b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d128b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d128b-135"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d128b-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d128b-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="d128b-136">Library</span></span><br/> | <dl> <span data-ttu-id="d128b-137"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d128b-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d128b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d128b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d128b-139">**IXml2Dex 介面**</span><span class="sxs-lookup"><span data-stu-id="d128b-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="d128b-140">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d128b-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




