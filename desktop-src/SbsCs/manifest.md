---
description: 資訊清單屬性是用來設定或取得主動啟用內容。
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx 資訊清單屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943345"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="519f8-103">ActCtx 資訊清單屬性</span><span class="sxs-lookup"><span data-stu-id="519f8-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="519f8-104">**資訊清單** 屬性是用來設定或取得主動啟用內容。</span><span class="sxs-lookup"><span data-stu-id="519f8-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="519f8-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="519f8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="519f8-106">語法</span><span class="sxs-lookup"><span data-stu-id="519f8-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="519f8-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="519f8-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="519f8-108">備註</span><span class="sxs-lookup"><span data-stu-id="519f8-108">Remarks</span></span>

<span data-ttu-id="519f8-109">如果可以使用提供的資訊清單檔來建立啟用內容，下列腳本會設定資訊清單屬性，並啟動資訊清單所指定的啟用常數。</span><span class="sxs-lookup"><span data-stu-id="519f8-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="519f8-110">如果無法從資訊清單建立啟用內容，啟用內容仍會設定為目前作用中的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="519f8-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="519f8-111">ActCtxObj。資訊清單 = "<*資訊清單檔案名*>";</span><span class="sxs-lookup"><span data-stu-id="519f8-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="519f8-112">如果先前已建立或啟用啟用內容，下列腳本會將 **資訊清單** 屬性設定為目前的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="519f8-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="519f8-113">如果先前未建立或啟用啟用內容，這會將 **資訊清單** 屬性設定為空字串。</span><span class="sxs-lookup"><span data-stu-id="519f8-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="519f8-114">"BSTR bstrManifest = ActCtxObj"</span><span class="sxs-lookup"><span data-stu-id="519f8-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="519f8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="519f8-115">Requirements</span></span>



| <span data-ttu-id="519f8-116">需求</span><span class="sxs-lookup"><span data-stu-id="519f8-116">Requirement</span></span> | <span data-ttu-id="519f8-117">值</span><span class="sxs-lookup"><span data-stu-id="519f8-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="519f8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="519f8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="519f8-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="519f8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="519f8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="519f8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="519f8-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="519f8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="519f8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="519f8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="519f8-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="519f8-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="519f8-124">IID</span><span class="sxs-lookup"><span data-stu-id="519f8-124">IID</span></span><br/>                      | <span data-ttu-id="519f8-125">IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="519f8-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




