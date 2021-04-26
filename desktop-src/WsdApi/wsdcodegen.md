---
description: 這是 WSDAPI 程式碼產生器 XML 腳本檔案的根項目。
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994675"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="c7e14-103">wsdCodeGen 元素</span><span class="sxs-lookup"><span data-stu-id="c7e14-103">wsdCodeGen element</span></span>

<span data-ttu-id="c7e14-104">這是 WSDAPI 程式碼產生器 XML 腳本檔案的根項目。</span><span class="sxs-lookup"><span data-stu-id="c7e14-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="c7e14-105">使用方式</span><span class="sxs-lookup"><span data-stu-id="c7e14-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="c7e14-106">屬性</span><span class="sxs-lookup"><span data-stu-id="c7e14-106">Attributes</span></span>



| <span data-ttu-id="c7e14-107">屬性</span><span class="sxs-lookup"><span data-stu-id="c7e14-107">Attribute</span></span>                        | <span data-ttu-id="c7e14-108">類型</span><span class="sxs-lookup"><span data-stu-id="c7e14-108">Type</span></span>                             | <span data-ttu-id="c7e14-109">必要</span><span class="sxs-lookup"><span data-stu-id="c7e14-109">Required</span></span>       | <span data-ttu-id="c7e14-110">描述</span><span class="sxs-lookup"><span data-stu-id="c7e14-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e14-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="c7e14-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="c7e14-112">任何字元字串。</span><span class="sxs-lookup"><span data-stu-id="c7e14-112">Any character string.</span></span><br/> | <span data-ttu-id="c7e14-113">Yes</span><span class="sxs-lookup"><span data-stu-id="c7e14-113">Yes</span></span><br/> | <span data-ttu-id="c7e14-114">設定檔案的版本。</span><span class="sxs-lookup"><span data-stu-id="c7e14-114">The version of the configuration file.</span></span> <span data-ttu-id="c7e14-115">唯一有效的值是 "1.0"。</span><span class="sxs-lookup"><span data-stu-id="c7e14-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c7e14-116">子元素</span><span class="sxs-lookup"><span data-stu-id="c7e14-116">Child elements</span></span>



| <span data-ttu-id="c7e14-117">元素</span><span class="sxs-lookup"><span data-stu-id="c7e14-117">Element</span></span>                                                         | <span data-ttu-id="c7e14-118">描述</span><span class="sxs-lookup"><span data-stu-id="c7e14-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7e14-119">**autoStatic**</span><span class="sxs-lookup"><span data-stu-id="c7e14-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="c7e14-120">指出 WsdCodeGen 是否應該嘗試自動將某些產生的欄位標記為靜態。</span><span class="sxs-lookup"><span data-stu-id="c7e14-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="c7e14-121">此選項預設為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="c7e14-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="c7e14-122">**檔**</span><span class="sxs-lookup"><span data-stu-id="c7e14-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="c7e14-123">指示程式碼產生器產生檔案。</span><span class="sxs-lookup"><span data-stu-id="c7e14-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="c7e14-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="c7e14-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="c7e14-125">要執行之裝置的裝載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c7e14-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="c7e14-126">此元素僅用於 (主機) 的裝置執行。</span><span class="sxs-lookup"><span data-stu-id="c7e14-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="c7e14-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="c7e14-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="c7e14-128">要產生的程式碼層數目。</span><span class="sxs-lookup"><span data-stu-id="c7e14-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="c7e14-129">在執行時間資料表中，會使用圖層編號來區分另一層程式碼。</span><span class="sxs-lookup"><span data-stu-id="c7e14-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="c7e14-130">WSDAPI 本身會使用產生的程式碼，其層號為0。</span><span class="sxs-lookup"><span data-stu-id="c7e14-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="c7e14-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="c7e14-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="c7e14-132">要在產生的程式碼中使用的前置詞，以確保產生的符號唯一性。</span><span class="sxs-lookup"><span data-stu-id="c7e14-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="c7e14-133">WSDAPI 使用 "WSD" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="c7e14-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="c7e14-134">**宏觀**</span><span class="sxs-lookup"><span data-stu-id="c7e14-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="c7e14-135">定義 [**include**](include.md) 元素要重複使用的 TEXT 或 CDATA。</span><span class="sxs-lookup"><span data-stu-id="c7e14-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="c7e14-136">**命名 空間**</span><span class="sxs-lookup"><span data-stu-id="c7e14-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="c7e14-137">描述要用於產生程式碼的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c7e14-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="c7e14-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="c7e14-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="c7e14-139">描述裝置的主機和託管中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c7e14-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="c7e14-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="c7e14-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="c7e14-141">要執行之裝置的製造商和型號中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c7e14-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="c7e14-142">此元素僅用於 (主機) 的裝置執行。</span><span class="sxs-lookup"><span data-stu-id="c7e14-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="c7e14-143">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="c7e14-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="c7e14-144">指定要針對合約資訊處理的 WSDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="c7e14-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="c7e14-145">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="c7e14-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="c7e14-146">指定要針對合約資訊處理的 XSD 檔案。</span><span class="sxs-lookup"><span data-stu-id="c7e14-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="c7e14-147">子項目順序</span><span class="sxs-lookup"><span data-stu-id="c7e14-147">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="c7e14-148">父元素</span><span class="sxs-lookup"><span data-stu-id="c7e14-148">Parent elements</span></span>

<span data-ttu-id="c7e14-149">沒有父元素。</span><span class="sxs-lookup"><span data-stu-id="c7e14-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e14-150">備註</span><span class="sxs-lookup"><span data-stu-id="c7e14-150">Remarks</span></span>

<span data-ttu-id="c7e14-151">一般情況下 [**，檔案**](file.md) 元素應該會在最後產生，因為它們會產生使用其他元素所指定之資料的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c7e14-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="c7e14-152">項目資訊</span><span class="sxs-lookup"><span data-stu-id="c7e14-152">Element information</span></span>



| <span data-ttu-id="c7e14-153">標籤</span><span class="sxs-lookup"><span data-stu-id="c7e14-153">Label</span></span> | <span data-ttu-id="c7e14-154">值</span><span class="sxs-lookup"><span data-stu-id="c7e14-154">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c7e14-155">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="c7e14-155">Minimum supported system</span></span><br/> | <span data-ttu-id="c7e14-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7e14-156">Windows Vista</span></span> |
| <span data-ttu-id="c7e14-157">可以是空的</span><span class="sxs-lookup"><span data-stu-id="c7e14-157">Can be empty</span></span>                        | <span data-ttu-id="c7e14-158">是</span><span class="sxs-lookup"><span data-stu-id="c7e14-158">Yes</span></span>           |



 

 




