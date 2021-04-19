---
description: ReadXMLFile 方法會載入 XML 專案檔。
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex：： ReadXMLFile 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983202"
---
# <a name="ixml2dexreadxmlfile-method"></a><span data-ttu-id="7d6a4-103">IXml2Dex：： ReadXMLFile 方法</span><span class="sxs-lookup"><span data-stu-id="7d6a4-103">IXml2Dex::ReadXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="7d6a4-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-104">\[Deprecated.</span></span> <span data-ttu-id="7d6a4-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7d6a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7d6a4-106">`ReadXMLFile`方法會載入 XML 專案檔。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-106">The `ReadXMLFile` method loads an XML project file.</span></span> <span data-ttu-id="7d6a4-107">這個方法會建立 XML 檔案中表示的所有物件的實例，並將其插入至時間軸，以及套用任何針對時間軸提供的屬性，例如畫面播放速率或預設效果。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-107">This method creates instances of all the objects expressed in the XML file and inserts them into the timeline, as well as applying any attributes given for the timeline, such as frame rate or default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6a4-108">語法</span><span class="sxs-lookup"><span data-stu-id="7d6a4-108">Syntax</span></span>


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a><span data-ttu-id="7d6a4-109">參數</span><span class="sxs-lookup"><span data-stu-id="7d6a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6a4-110">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="7d6a4-110">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a4-111">時間軸物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-111">Pointer to a timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="7d6a4-112">*XMLName*</span><span class="sxs-lookup"><span data-stu-id="7d6a4-112">*XMLName*</span></span> 
</dt> <dd>

<span data-ttu-id="7d6a4-113">字串，指定要載入的檔案名。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-113">String that specifies the name of the file to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6a4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d6a4-114">Return value</span></span>

<span data-ttu-id="7d6a4-115">傳回 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-115">Returns an HRESULT value.</span></span> <span data-ttu-id="7d6a4-116">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-116">Possible values include the following.</span></span>



| <span data-ttu-id="7d6a4-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7d6a4-117">Return code</span></span>                                                                                                  | <span data-ttu-id="7d6a4-118">Description</span><span class="sxs-lookup"><span data-stu-id="7d6a4-118">Description</span></span>                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="7d6a4-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a4-119"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="7d6a4-120">Success</span><span class="sxs-lookup"><span data-stu-id="7d6a4-120">Success</span></span><br/>             |
| <dl> <span data-ttu-id="7d6a4-121"><dt>**VFW \_ E \_ 不正確 \_ 檔 \_ 格式**</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a4-121"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="7d6a4-122">不正確檔案格式</span><span class="sxs-lookup"><span data-stu-id="7d6a4-122">Invalid file format</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d6a4-123">備註</span><span class="sxs-lookup"><span data-stu-id="7d6a4-123">Remarks</span></span>

<span data-ttu-id="7d6a4-124">這個方法不會在插入 XML 檔案中定義的新物件之前，從時間軸清除現有的物件。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-124">This method does not clear existing objects from the timeline before it inserts the new objects defined in the XML file.</span></span> <span data-ttu-id="7d6a4-125">如果您需要重新整理現有的時間軸，請先呼叫 [**IAMTimeline：： ClearAllGroups**](iamtimeline-clearallgroups.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-125">If you need to refresh an existing timeline, call [**IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) first.</span></span>

> [!Note]  
> <span data-ttu-id="7d6a4-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7d6a4-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7d6a4-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7d6a4-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d6a4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d6a4-129">Requirements</span></span>



| <span data-ttu-id="7d6a4-130">需求</span><span class="sxs-lookup"><span data-stu-id="7d6a4-130">Requirement</span></span> | <span data-ttu-id="7d6a4-131">值</span><span class="sxs-lookup"><span data-stu-id="7d6a4-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6a4-132">版本</span><span class="sxs-lookup"><span data-stu-id="7d6a4-132">Version</span></span><br/> | <span data-ttu-id="7d6a4-133">Internet Explorer 4.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7d6a4-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="7d6a4-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7d6a4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7d6a4-135"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a4-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d6a4-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d6a4-136">Library</span></span><br/> | <dl> <span data-ttu-id="7d6a4-137"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a4-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d6a4-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d6a4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6a4-139">**IXml2Dex 介面**</span><span class="sxs-lookup"><span data-stu-id="7d6a4-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="7d6a4-140">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="7d6a4-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




