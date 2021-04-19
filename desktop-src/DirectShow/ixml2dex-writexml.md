---
description: WriteXML 方法會將時間軸轉譯為 XML 字串。
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex：： WriteXML 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995625"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="674e0-103">IXml2Dex：： WriteXML 方法</span><span class="sxs-lookup"><span data-stu-id="674e0-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="674e0-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="674e0-104">\[Deprecated.</span></span> <span data-ttu-id="674e0-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="674e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="674e0-106">方法會將 `WriteXML` 時間軸轉譯為 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="674e0-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="674e0-107">語法</span><span class="sxs-lookup"><span data-stu-id="674e0-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="674e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="674e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674e0-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="674e0-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="674e0-110">時間軸物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="674e0-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="674e0-111">*pbstrXML*</span><span class="sxs-lookup"><span data-stu-id="674e0-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="674e0-112">BSTR 類型變數的指標，此變數會接收描述時間軸的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="674e0-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="674e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="674e0-113">Return value</span></span>

<span data-ttu-id="674e0-114">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="674e0-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="674e0-115">如果沒有足夠的記憶體可進行轉換，則會傳回 E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="674e0-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="674e0-116">否則，會傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="674e0-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="674e0-117">備註</span><span class="sxs-lookup"><span data-stu-id="674e0-117">Remarks</span></span>

<span data-ttu-id="674e0-118">方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="674e0-118">The method allocates memory for the string.</span></span> <span data-ttu-id="674e0-119">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="674e0-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="674e0-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="674e0-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="674e0-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="674e0-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="674e0-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="674e0-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="674e0-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="674e0-123">Requirements</span></span>



| <span data-ttu-id="674e0-124">需求</span><span class="sxs-lookup"><span data-stu-id="674e0-124">Requirement</span></span> | <span data-ttu-id="674e0-125">值</span><span class="sxs-lookup"><span data-stu-id="674e0-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="674e0-126">版本</span><span class="sxs-lookup"><span data-stu-id="674e0-126">Version</span></span><br/> | <span data-ttu-id="674e0-127">Internet Explorer 4.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="674e0-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="674e0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="674e0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="674e0-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="674e0-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="674e0-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="674e0-130">Library</span></span><br/> | <dl> <span data-ttu-id="674e0-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="674e0-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674e0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="674e0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674e0-133">**IXml2Dex 介面**</span><span class="sxs-lookup"><span data-stu-id="674e0-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="674e0-134">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="674e0-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




