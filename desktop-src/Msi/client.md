---
description: 用戶端物件代表元件和用戶端產品之間的關聯性。
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: 用戶端物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993357"
---
# <a name="client-object"></a><span data-ttu-id="2c203-103">用戶端物件</span><span class="sxs-lookup"><span data-stu-id="2c203-103">Client object</span></span>

<span data-ttu-id="2c203-104">用戶端物件代表元件和用戶端產品之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="2c203-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="2c203-105">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="2c203-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="2c203-106">從 Windows Installer 5.0 開始，可以使用這個物件。</span><span class="sxs-lookup"><span data-stu-id="2c203-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="2c203-107">成員</span><span class="sxs-lookup"><span data-stu-id="2c203-107">Members</span></span>

<span data-ttu-id="2c203-108">**用戶端** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c203-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="2c203-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2c203-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c203-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2c203-110">Properties</span></span>

<span data-ttu-id="2c203-111">**用戶端** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c203-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="2c203-112">屬性</span><span class="sxs-lookup"><span data-stu-id="2c203-112">Property</span></span>                                                 | <span data-ttu-id="2c203-113">描述</span><span class="sxs-lookup"><span data-stu-id="2c203-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="2c203-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="2c203-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="2c203-115">有問題之元件的元件代碼。</span><span class="sxs-lookup"><span data-stu-id="2c203-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="2c203-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="2c203-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="2c203-117">產品的內容。</span><span class="sxs-lookup"><span data-stu-id="2c203-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="2c203-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="2c203-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="2c203-119">有問題之元件的用戶端產品。</span><span class="sxs-lookup"><span data-stu-id="2c203-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="2c203-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="2c203-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="2c203-121">元件的使用者 SID。</span><span class="sxs-lookup"><span data-stu-id="2c203-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2c203-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c203-122">Requirements</span></span>



| <span data-ttu-id="2c203-123">需求</span><span class="sxs-lookup"><span data-stu-id="2c203-123">Requirement</span></span> | <span data-ttu-id="2c203-124">值</span><span class="sxs-lookup"><span data-stu-id="2c203-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c203-125">版本</span><span class="sxs-lookup"><span data-stu-id="2c203-125">Version</span></span><br/> | <span data-ttu-id="2c203-126">Windows Installer 5.0 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2c203-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="2c203-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2c203-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c203-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c203-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c203-129">IID</span><span class="sxs-lookup"><span data-stu-id="2c203-129">IID</span></span><br/>     | <span data-ttu-id="2c203-130">IID \_ IClient 定義為000C1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2c203-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="2c203-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c203-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c203-132">使用 Automation 介面</span><span class="sxs-lookup"><span data-stu-id="2c203-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="2c203-133">Windows Installer 腳本範例</span><span class="sxs-lookup"><span data-stu-id="2c203-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




