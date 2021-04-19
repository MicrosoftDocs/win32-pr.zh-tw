---
description: ComponentInfo 物件代表可透過從 MsiGetComponentPathEx 呼叫取得之元件的其他詳細資料。
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: ComponentInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994696"
---
# <a name="componentinfo-object"></a><span data-ttu-id="62ee7-103">ComponentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="62ee7-103">ComponentInfo object</span></span>

<span data-ttu-id="62ee7-104">ComponentInfo 物件代表可透過從 MsiGetComponentPathEx 呼叫取得之元件的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="62ee7-104">The ComponentInfo object represents additional details about a component that may be obtained via a call from MsiGetComponentPathEx.</span></span>

<span data-ttu-id="62ee7-105">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="62ee7-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="62ee7-106">從 Windows Installer 5.0 開始，可以使用這個物件。</span><span class="sxs-lookup"><span data-stu-id="62ee7-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="62ee7-107">成員</span><span class="sxs-lookup"><span data-stu-id="62ee7-107">Members</span></span>

<span data-ttu-id="62ee7-108">**ComponentInfo** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="62ee7-108">The **ComponentInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="62ee7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="62ee7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62ee7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="62ee7-110">Properties</span></span>

<span data-ttu-id="62ee7-111">**ComponentInfo** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62ee7-111">The **ComponentInfo** object has these properties.</span></span>



| <span data-ttu-id="62ee7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="62ee7-112">Property</span></span>                                                        | <span data-ttu-id="62ee7-113">描述</span><span class="sxs-lookup"><span data-stu-id="62ee7-113">Description</span></span>                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="62ee7-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="62ee7-114">**ComponentCode**</span></span>](componentinfo-componentcode.md)<br/> | <span data-ttu-id="62ee7-115">有問題之元件的元件代碼。</span><span class="sxs-lookup"><span data-stu-id="62ee7-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="62ee7-116">**路徑**</span><span class="sxs-lookup"><span data-stu-id="62ee7-116">**Path**</span></span>](componentinfo-componentcode.md)<br/>          | <span data-ttu-id="62ee7-117">元件的路徑。</span><span class="sxs-lookup"><span data-stu-id="62ee7-117">The path of the component.</span></span><br/>                       |
| [<span data-ttu-id="62ee7-118">**狀態**</span><span class="sxs-lookup"><span data-stu-id="62ee7-118">**State**</span></span>](componentinfo-state.md)<br/>                 | <span data-ttu-id="62ee7-119">元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="62ee7-119">The state of the component.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="62ee7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="62ee7-120">Requirements</span></span>



| <span data-ttu-id="62ee7-121">需求</span><span class="sxs-lookup"><span data-stu-id="62ee7-121">Requirement</span></span> | <span data-ttu-id="62ee7-122">值</span><span class="sxs-lookup"><span data-stu-id="62ee7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62ee7-123">版本</span><span class="sxs-lookup"><span data-stu-id="62ee7-123">Version</span></span><br/> | <span data-ttu-id="62ee7-124">Windows Installer 5.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="62ee7-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="62ee7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="62ee7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="62ee7-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ee7-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="62ee7-127">IID</span><span class="sxs-lookup"><span data-stu-id="62ee7-127">IID</span></span><br/>     | <span data-ttu-id="62ee7-128">IID \_ IComponentInfo 定義為000C1099-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="62ee7-128">IID\_IComponentInfo is defined as 000C1099-0000-0000-C000-000000000046</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="62ee7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62ee7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ee7-130">使用 Automation 介面</span><span class="sxs-lookup"><span data-stu-id="62ee7-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="62ee7-131">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="62ee7-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




