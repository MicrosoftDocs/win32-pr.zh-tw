---
description: Component 物件代表可供列舉之元件的唯一實例。
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: 元件物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994290"
---
# <a name="component-object"></a><span data-ttu-id="928f2-103">元件物件</span><span class="sxs-lookup"><span data-stu-id="928f2-103">Component object</span></span>

<span data-ttu-id="928f2-104">Component 物件代表可供列舉之元件的唯一實例。</span><span class="sxs-lookup"><span data-stu-id="928f2-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="928f2-105">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="928f2-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="928f2-106">從 Windows Installer 5.0 開始，可以使用這個物件。</span><span class="sxs-lookup"><span data-stu-id="928f2-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="928f2-107">成員</span><span class="sxs-lookup"><span data-stu-id="928f2-107">Members</span></span>

<span data-ttu-id="928f2-108">**元件** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="928f2-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="928f2-109">屬性</span><span class="sxs-lookup"><span data-stu-id="928f2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="928f2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="928f2-110">Properties</span></span>

<span data-ttu-id="928f2-111">**元件** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="928f2-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="928f2-112">屬性</span><span class="sxs-lookup"><span data-stu-id="928f2-112">Property</span></span>                                                    | <span data-ttu-id="928f2-113">描述</span><span class="sxs-lookup"><span data-stu-id="928f2-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="928f2-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="928f2-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="928f2-115">有問題之元件的元件代碼。</span><span class="sxs-lookup"><span data-stu-id="928f2-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="928f2-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="928f2-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="928f2-117">判斷為適用于問題元件的內容。</span><span class="sxs-lookup"><span data-stu-id="928f2-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="928f2-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="928f2-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="928f2-119">列舉元件的使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="928f2-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="928f2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="928f2-120">Requirements</span></span>



| <span data-ttu-id="928f2-121">需求</span><span class="sxs-lookup"><span data-stu-id="928f2-121">Requirement</span></span> | <span data-ttu-id="928f2-122">值</span><span class="sxs-lookup"><span data-stu-id="928f2-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="928f2-123">版本</span><span class="sxs-lookup"><span data-stu-id="928f2-123">Version</span></span><br/> | <span data-ttu-id="928f2-124">Windows Installer 5.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="928f2-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="928f2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="928f2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="928f2-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="928f2-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="928f2-127">IID</span><span class="sxs-lookup"><span data-stu-id="928f2-127">IID</span></span><br/>     | <span data-ttu-id="928f2-128">IID \_ IComponent 定義為000C1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="928f2-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="928f2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="928f2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="928f2-130">使用 Automation 介面</span><span class="sxs-lookup"><span data-stu-id="928f2-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="928f2-131">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="928f2-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




