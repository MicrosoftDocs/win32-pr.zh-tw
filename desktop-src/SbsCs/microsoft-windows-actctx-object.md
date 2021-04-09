---
description: ActCtx 物件參考資訊清單，並提供一種方法讓腳本引擎存取並存元件。 ActCtx 物件可以用來建立與 COM 元件並存元件的實例，以供使用。
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: ActCtx 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848838"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="de7c1-104">ActCtx 物件</span><span class="sxs-lookup"><span data-stu-id="de7c1-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="de7c1-105">**ActCtx** 物件參考資訊清單，並提供一種方法讓腳本引擎存取並存元件。</span><span class="sxs-lookup"><span data-stu-id="de7c1-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="de7c1-106">**ActCtx** 物件可以用來建立與 COM 元件並存元件的實例，以供使用。</span><span class="sxs-lookup"><span data-stu-id="de7c1-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="de7c1-107">**ActCtx** 物件是 windows Server 2003 中的元件。</span><span class="sxs-lookup"><span data-stu-id="de7c1-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="de7c1-108">它也可以由使用 Windows Installer 進行安裝程式的應用程式安裝，並在其安裝套件中包含為合併模組。</span><span class="sxs-lookup"><span data-stu-id="de7c1-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="de7c1-109">成員</span><span class="sxs-lookup"><span data-stu-id="de7c1-109">Members</span></span>

<span data-ttu-id="de7c1-110">**ActCtx** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="de7c1-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="de7c1-111">方法</span><span class="sxs-lookup"><span data-stu-id="de7c1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="de7c1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="de7c1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="de7c1-113">方法</span><span class="sxs-lookup"><span data-stu-id="de7c1-113">Methods</span></span>

<span data-ttu-id="de7c1-114">**ActCtx** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="de7c1-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="de7c1-115">方法</span><span class="sxs-lookup"><span data-stu-id="de7c1-115">Method</span></span>                               | <span data-ttu-id="de7c1-116">描述</span><span class="sxs-lookup"><span data-stu-id="de7c1-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="de7c1-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="de7c1-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="de7c1-118">在目前資訊清單的內容中建立物件。</span><span class="sxs-lookup"><span data-stu-id="de7c1-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="de7c1-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="de7c1-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="de7c1-120">取得現有 **ActCtx** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="de7c1-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="de7c1-121">屬性</span><span class="sxs-lookup"><span data-stu-id="de7c1-121">Properties</span></span>

<span data-ttu-id="de7c1-122">**ActCtx** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="de7c1-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="de7c1-123">屬性</span><span class="sxs-lookup"><span data-stu-id="de7c1-123">Property</span></span>                                | <span data-ttu-id="de7c1-124">存取類型</span><span class="sxs-lookup"><span data-stu-id="de7c1-124">Access type</span></span>          | <span data-ttu-id="de7c1-125">Description</span><span class="sxs-lookup"><span data-stu-id="de7c1-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="de7c1-126">**清單**</span><span class="sxs-lookup"><span data-stu-id="de7c1-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="de7c1-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="de7c1-127">Read-only</span></span><br/> | <span data-ttu-id="de7c1-128">取得有效的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="de7c1-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="de7c1-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="de7c1-129">Requirements</span></span>



| <span data-ttu-id="de7c1-130">需求</span><span class="sxs-lookup"><span data-stu-id="de7c1-130">Requirement</span></span> | <span data-ttu-id="de7c1-131">值</span><span class="sxs-lookup"><span data-stu-id="de7c1-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de7c1-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de7c1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="de7c1-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de7c1-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="de7c1-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de7c1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="de7c1-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de7c1-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




