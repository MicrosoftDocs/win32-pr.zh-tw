---
title: LevelType 複雜類型
description: 定義嚴重性值，判斷所記錄事件的詳細程度。
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- LevelType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093883"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="27fbd-104">LevelType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="27fbd-104">LevelType Complex Type</span></span>

<span data-ttu-id="27fbd-105">定義嚴重性值，判斷所記錄事件的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="27fbd-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="27fbd-106">屬性</span><span class="sxs-lookup"><span data-stu-id="27fbd-106">Attributes</span></span>



| <span data-ttu-id="27fbd-107">名稱</span><span class="sxs-lookup"><span data-stu-id="27fbd-107">Name</span></span>    | <span data-ttu-id="27fbd-108">類型</span><span class="sxs-lookup"><span data-stu-id="27fbd-108">Type</span></span>                                                              | <span data-ttu-id="27fbd-109">Description</span><span class="sxs-lookup"><span data-stu-id="27fbd-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27fbd-110">message</span><span class="sxs-lookup"><span data-stu-id="27fbd-110">message</span></span> | [<span data-ttu-id="27fbd-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="27fbd-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="27fbd-112">層級的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="27fbd-112">The localized display name for the level.</span></span> <span data-ttu-id="27fbd-113">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="27fbd-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="27fbd-114">NAME</span><span class="sxs-lookup"><span data-stu-id="27fbd-114">name</span></span>    | <span data-ttu-id="27fbd-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="27fbd-115">**QName**</span></span>                                                         | <span data-ttu-id="27fbd-116">要指派給這個層級的名稱。</span><span class="sxs-lookup"><span data-stu-id="27fbd-116">The name to assign to this level.</span></span> <span data-ttu-id="27fbd-117">這個名稱在提供者的範圍內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="27fbd-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="27fbd-118">符號</span><span class="sxs-lookup"><span data-stu-id="27fbd-118">symbol</span></span>  | [<span data-ttu-id="27fbd-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="27fbd-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="27fbd-120">用來參考應用程式中之層級的符號。</span><span class="sxs-lookup"><span data-stu-id="27fbd-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="27fbd-121">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立層級的常數。</span><span class="sxs-lookup"><span data-stu-id="27fbd-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="27fbd-122">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="27fbd-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="27fbd-123">value</span><span class="sxs-lookup"><span data-stu-id="27fbd-123">value</span></span>   | [<span data-ttu-id="27fbd-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="27fbd-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="27fbd-125">層級值。</span><span class="sxs-lookup"><span data-stu-id="27fbd-125">The level value.</span></span> <span data-ttu-id="27fbd-126">您可以指定範圍16到255之間的值。</span><span class="sxs-lookup"><span data-stu-id="27fbd-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="27fbd-127">如需預先定義的層級值，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="27fbd-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="27fbd-128">備註</span><span class="sxs-lookup"><span data-stu-id="27fbd-128">Remarks</span></span>

<span data-ttu-id="27fbd-129">以下是您可以使用的預先定義層級值。</span><span class="sxs-lookup"><span data-stu-id="27fbd-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="27fbd-130">這些值是在包含于 Windows SDK 的 Winmeta.xml 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="27fbd-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="27fbd-131">Name</span><span class="sxs-lookup"><span data-stu-id="27fbd-131">Name</span></span>              | <span data-ttu-id="27fbd-132">值</span><span class="sxs-lookup"><span data-stu-id="27fbd-132">Value</span></span> | <span data-ttu-id="27fbd-133">符號</span><span class="sxs-lookup"><span data-stu-id="27fbd-133">Symbol</span></span>                    | <span data-ttu-id="27fbd-134">描述</span><span class="sxs-lookup"><span data-stu-id="27fbd-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="27fbd-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="27fbd-135">win:Critical</span></span>      | <span data-ttu-id="27fbd-136">1</span><span class="sxs-lookup"><span data-stu-id="27fbd-136">1</span></span>     | <span data-ttu-id="27fbd-137">NEW-WINEVENT \_ 層級 \_ 重大</span><span class="sxs-lookup"><span data-stu-id="27fbd-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="27fbd-138">識別異常離開或終止事件。</span><span class="sxs-lookup"><span data-stu-id="27fbd-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="27fbd-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="27fbd-139">win:Error</span></span>         | <span data-ttu-id="27fbd-140">2</span><span class="sxs-lookup"><span data-stu-id="27fbd-140">2</span></span>     | <span data-ttu-id="27fbd-141">NEW-WINEVENT \_ 層級 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="27fbd-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="27fbd-142">識別嚴重的錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="27fbd-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="27fbd-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="27fbd-143">win:Warning</span></span>       | <span data-ttu-id="27fbd-144">3</span><span class="sxs-lookup"><span data-stu-id="27fbd-144">3</span></span>     | <span data-ttu-id="27fbd-145">NEW-WINEVENT \_ 層級 \_ 警告</span><span class="sxs-lookup"><span data-stu-id="27fbd-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="27fbd-146">識別如配置失敗的警告事件。</span><span class="sxs-lookup"><span data-stu-id="27fbd-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="27fbd-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="27fbd-147">win:Informational</span></span> | <span data-ttu-id="27fbd-148">4</span><span class="sxs-lookup"><span data-stu-id="27fbd-148">4</span></span>     | <span data-ttu-id="27fbd-149">NEW-WINEVENT \_ 層級 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="27fbd-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="27fbd-150">識別非錯誤事件，例如進入或離開事件。</span><span class="sxs-lookup"><span data-stu-id="27fbd-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="27fbd-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="27fbd-151">win:Verbose</span></span>       | <span data-ttu-id="27fbd-152">5</span><span class="sxs-lookup"><span data-stu-id="27fbd-152">5</span></span>     | <span data-ttu-id="27fbd-153">NEW-WINEVENT \_ 層級 \_ 詳細資訊</span><span class="sxs-lookup"><span data-stu-id="27fbd-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="27fbd-154">識別詳細的追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="27fbd-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="27fbd-155">較高的數位表示您也可以取得較低的層級。</span><span class="sxs-lookup"><span data-stu-id="27fbd-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="27fbd-156">例如，如果您指定「win：警告」，則會收到所有警告、錯誤和重大事件。</span><span class="sxs-lookup"><span data-stu-id="27fbd-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="27fbd-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="27fbd-157">Requirements</span></span>



| <span data-ttu-id="27fbd-158">需求</span><span class="sxs-lookup"><span data-stu-id="27fbd-158">Requirement</span></span> | <span data-ttu-id="27fbd-159">值</span><span class="sxs-lookup"><span data-stu-id="27fbd-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27fbd-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27fbd-160">Minimum supported client</span></span><br/> | <span data-ttu-id="27fbd-161">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27fbd-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27fbd-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27fbd-162">Minimum supported server</span></span><br/> | <span data-ttu-id="27fbd-163">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27fbd-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





