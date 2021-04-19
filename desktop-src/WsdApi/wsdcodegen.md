---
description: 這是 WSDAPI 程式碼產生器 XML 腳本檔案的根項目。
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999872"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="2b757-103">wsdCodeGen 元素</span><span class="sxs-lookup"><span data-stu-id="2b757-103">wsdCodeGen element</span></span>

<span data-ttu-id="2b757-104">這是 WSDAPI 程式碼產生器 XML 腳本檔案的根項目。</span><span class="sxs-lookup"><span data-stu-id="2b757-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="2b757-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="2b757-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="2b757-106">屬性</span><span class="sxs-lookup"><span data-stu-id="2b757-106">Attributes</span></span>



| <span data-ttu-id="2b757-107">屬性</span><span class="sxs-lookup"><span data-stu-id="2b757-107">Attribute</span></span>                        | <span data-ttu-id="2b757-108">類型</span><span class="sxs-lookup"><span data-stu-id="2b757-108">Type</span></span>                             | <span data-ttu-id="2b757-109">必要</span><span class="sxs-lookup"><span data-stu-id="2b757-109">Required</span></span>       | <span data-ttu-id="2b757-110">描述</span><span class="sxs-lookup"><span data-stu-id="2b757-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b757-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="2b757-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="2b757-112">任何字元字串。</span><span class="sxs-lookup"><span data-stu-id="2b757-112">Any character string.</span></span><br/> | <span data-ttu-id="2b757-113">Yes</span><span class="sxs-lookup"><span data-stu-id="2b757-113">Yes</span></span><br/> | <span data-ttu-id="2b757-114">設定檔案的版本。</span><span class="sxs-lookup"><span data-stu-id="2b757-114">The version of the configuration file.</span></span> <span data-ttu-id="2b757-115">唯一有效的值是 "1.0"。</span><span class="sxs-lookup"><span data-stu-id="2b757-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="2b757-116">子元素</span><span class="sxs-lookup"><span data-stu-id="2b757-116">Child elements</span></span>



| <span data-ttu-id="2b757-117">元素</span><span class="sxs-lookup"><span data-stu-id="2b757-117">Element</span></span>                                                         | <span data-ttu-id="2b757-118">描述</span><span class="sxs-lookup"><span data-stu-id="2b757-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b757-119">**autoStatic**</span><span class="sxs-lookup"><span data-stu-id="2b757-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="2b757-120">指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。</span><span class="sxs-lookup"><span data-stu-id="2b757-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="2b757-121">此選項預設為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="2b757-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="2b757-122">**檔**</span><span class="sxs-lookup"><span data-stu-id="2b757-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="2b757-123">指示程式碼產生器產生檔案。</span><span class="sxs-lookup"><span data-stu-id="2b757-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="2b757-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="2b757-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="2b757-125">要執行之裝置的裝載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2b757-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="2b757-126">此元素僅用於 (主機) 的裝置執行。</span><span class="sxs-lookup"><span data-stu-id="2b757-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="2b757-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="2b757-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="2b757-128">要產生的程式碼層數目。</span><span class="sxs-lookup"><span data-stu-id="2b757-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="2b757-129">在執行時間資料表中，會使用圖層編號來區分另一層程式碼。</span><span class="sxs-lookup"><span data-stu-id="2b757-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="2b757-130">WSDAPI 本身會使用產生的程式碼，其層號為0。</span><span class="sxs-lookup"><span data-stu-id="2b757-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="2b757-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="2b757-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="2b757-132">要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。</span><span class="sxs-lookup"><span data-stu-id="2b757-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="2b757-133">WSDAPI 使用 "WSD" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="2b757-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="2b757-134">**宏觀**</span><span class="sxs-lookup"><span data-stu-id="2b757-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="2b757-135">定義 [**include**](include.md) 元素要重複使用的 TEXT 或 CDATA。</span><span class="sxs-lookup"><span data-stu-id="2b757-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="2b757-136">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="2b757-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="2b757-137">描述要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="2b757-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="2b757-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="2b757-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="2b757-139">描述裝置的主機和託管中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2b757-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="2b757-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="2b757-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="2b757-141">要執行之裝置的製造商和型號中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2b757-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="2b757-142">此元素僅用於 (主機) 的裝置執行。</span><span class="sxs-lookup"><span data-stu-id="2b757-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="2b757-143">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="2b757-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="2b757-144">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="2b757-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="2b757-145">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="2b757-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="2b757-146">指定要針對合約資訊處理的 XSD 檔案。</span><span class="sxs-lookup"><span data-stu-id="2b757-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="2b757-147">子項目順序</span><span class="sxs-lookup"><span data-stu-id="2b757-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="2b757-148">父元素</span><span class="sxs-lookup"><span data-stu-id="2b757-148">Parent elements</span></span>

<span data-ttu-id="2b757-149">沒有父元素。</span><span class="sxs-lookup"><span data-stu-id="2b757-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b757-150">備註</span><span class="sxs-lookup"><span data-stu-id="2b757-150">Remarks</span></span>

<span data-ttu-id="2b757-151">一般情況下 [**，檔案**](file.md) 元素應該會在最後產生，因為它們會產生使用其他元素所指定之資料的程式碼。</span><span class="sxs-lookup"><span data-stu-id="2b757-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="2b757-152">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2b757-152">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2b757-153">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="2b757-153">Minimum supported system</span></span><br/> | <span data-ttu-id="2b757-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b757-154">Windows Vista</span></span> |
| <span data-ttu-id="2b757-155">可以是空的</span><span class="sxs-lookup"><span data-stu-id="2b757-155">Can be empty</span></span>                        | <span data-ttu-id="2b757-156">是</span><span class="sxs-lookup"><span data-stu-id="2b757-156">Yes</span></span>           |



 

 




