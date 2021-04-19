---
description: IXml2Dex 介面會將 DirectShow 編輯服務 (DES) 專案檔儲存並載入可延伸標記語言 (XML)  (XML) 。 此介面也提供讀取和寫入 DirectShow 圖形 ( grf) 檔案的方法。
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: 'IXml2Dex 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979565"
---
# <a name="ixml2dex-interface"></a><span data-ttu-id="90cc3-104">IXml2Dex 介面</span><span class="sxs-lookup"><span data-stu-id="90cc3-104">IXml2Dex interface</span></span>

> [!Note]  
> <span data-ttu-id="90cc3-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="90cc3-105">\[Deprecated.</span></span> <span data-ttu-id="90cc3-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="90cc3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="90cc3-107">`IXml2Dex`介面會在可延伸標記語言 (XML)  (XML) 中儲存及載入[DirectShow 編輯服務](directshow-editing-services.md) (DES) 專案檔。</span><span class="sxs-lookup"><span data-stu-id="90cc3-107">The `IXml2Dex` interface saves and loads [DirectShow Editing Services](directshow-editing-services.md) (DES) project files in Extensible Markup Language (XML).</span></span> <span data-ttu-id="90cc3-108">此介面也提供讀取和寫入 DirectShow 圖形 ( grf) 檔案的方法。</span><span class="sxs-lookup"><span data-stu-id="90cc3-108">This interface also provides methods for reading and writing DirectShow graph (.grf) files.</span></span>

## <a name="members"></a><span data-ttu-id="90cc3-109">成員</span><span class="sxs-lookup"><span data-stu-id="90cc3-109">Members</span></span>

<span data-ttu-id="90cc3-110">**IXml2Dex** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="90cc3-110">The **IXml2Dex** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="90cc3-111">**IXml2Dex** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="90cc3-111">**IXml2Dex** also has these types of members:</span></span>

-   [<span data-ttu-id="90cc3-112">方法</span><span class="sxs-lookup"><span data-stu-id="90cc3-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="90cc3-113">方法</span><span class="sxs-lookup"><span data-stu-id="90cc3-113">Methods</span></span>

<span data-ttu-id="90cc3-114">**IXml2Dex** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="90cc3-114">The **IXml2Dex** interface has these methods.</span></span>



| <span data-ttu-id="90cc3-115">方法</span><span class="sxs-lookup"><span data-stu-id="90cc3-115">Method</span></span>                                                      | <span data-ttu-id="90cc3-116">描述</span><span class="sxs-lookup"><span data-stu-id="90cc3-116">Description</span></span>                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="90cc3-117">**CopyXML**</span><span class="sxs-lookup"><span data-stu-id="90cc3-117">**CopyXML**</span></span>](ixml2dex-copyxml.md)                         | <span data-ttu-id="90cc3-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-118">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-119">**CreateGraphFromFile**</span><span class="sxs-lookup"><span data-stu-id="90cc3-119">**CreateGraphFromFile**</span></span>](ixml2dex-creategraphfromfile.md) | <span data-ttu-id="90cc3-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-120">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-121">**刪除**</span><span class="sxs-lookup"><span data-stu-id="90cc3-121">**Delete**</span></span>](ixml2dex-delete.md)                           | <span data-ttu-id="90cc3-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-122">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-123">**PasteXML**</span><span class="sxs-lookup"><span data-stu-id="90cc3-123">**PasteXML**</span></span>](ixml2dex-pastexml.md)                       | <span data-ttu-id="90cc3-124">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-124">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-125">**PasteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="90cc3-125">**PasteXMLFile**</span></span>](ixml2dex-pastexmlfile.md)               | <span data-ttu-id="90cc3-126">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-126">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-127">**ReadXML**</span><span class="sxs-lookup"><span data-stu-id="90cc3-127">**ReadXML**</span></span>](ixml2dex-readxml.md)                         | <span data-ttu-id="90cc3-128">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-128">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-129">**ReadXMLFile**</span><span class="sxs-lookup"><span data-stu-id="90cc3-129">**ReadXMLFile**</span></span>](ixml2dex-readxmlfile.md)                 | <span data-ttu-id="90cc3-130">載入 XML 專案檔。</span><span class="sxs-lookup"><span data-stu-id="90cc3-130">Loads an XML project file.</span></span><br/>                                      |
| [<span data-ttu-id="90cc3-131">**重設**</span><span class="sxs-lookup"><span data-stu-id="90cc3-131">**Reset**</span></span>](ixml2dex-reset.md)                             | <span data-ttu-id="90cc3-132">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-132">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="90cc3-133">**WriteGrfFile**</span><span class="sxs-lookup"><span data-stu-id="90cc3-133">**WriteGrfFile**</span></span>](ixml2dex-writegrffile.md)               | <span data-ttu-id="90cc3-134">將篩選圖形寫入 grf 格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="90cc3-134">Writes a filter graph to a file in .grf format.</span></span><br/>                 |
| [<span data-ttu-id="90cc3-135">**WriteXML**</span><span class="sxs-lookup"><span data-stu-id="90cc3-135">**WriteXML**</span></span>](ixml2dex-writexml.md)                       | <span data-ttu-id="90cc3-136">將時間軸轉譯為 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="90cc3-136">Translates a timeline to an XML string.</span></span><br/>                         |
| [<span data-ttu-id="90cc3-137">**WriteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="90cc3-137">**WriteXMLFile**</span></span>](ixml2dex-writexmlfile.md)               | <span data-ttu-id="90cc3-138">將時間軸轉譯成 XML，並將 XML 資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="90cc3-138">Translates a timeline to XML and writes the XML data to a file.</span></span><br/> |
| [<span data-ttu-id="90cc3-139">**WriteXMLPart**</span><span class="sxs-lookup"><span data-stu-id="90cc3-139">**WriteXMLPart**</span></span>](ixml2dex-writexmlpart.md)               | <span data-ttu-id="90cc3-140">未實作。</span><span class="sxs-lookup"><span data-stu-id="90cc3-140">Not implemented.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="90cc3-141">備註</span><span class="sxs-lookup"><span data-stu-id="90cc3-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="90cc3-142">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="90cc3-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="90cc3-143">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="90cc3-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="90cc3-144">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="90cc3-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90cc3-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="90cc3-145">Requirements</span></span>



| <span data-ttu-id="90cc3-146">需求</span><span class="sxs-lookup"><span data-stu-id="90cc3-146">Requirement</span></span> | <span data-ttu-id="90cc3-147">值</span><span class="sxs-lookup"><span data-stu-id="90cc3-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90cc3-148">版本</span><span class="sxs-lookup"><span data-stu-id="90cc3-148">Version</span></span><br/> | <span data-ttu-id="90cc3-149">Internet Explorer 4.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="90cc3-149">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="90cc3-150">標頭</span><span class="sxs-lookup"><span data-stu-id="90cc3-150">Header</span></span><br/>  | <dl> <span data-ttu-id="90cc3-151"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="90cc3-151"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="90cc3-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="90cc3-152">Library</span></span><br/> | <dl> <span data-ttu-id="90cc3-153"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90cc3-153"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
