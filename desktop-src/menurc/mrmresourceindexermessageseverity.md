---
title: 'MrmResourceIndexerMessageSeverity 列舉 (MrmResourceIndexer) '
description: 定義常數，指定資源索引子訊息的嚴重性。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- MrmResourceIndexerMessageSeverity 列舉功能表和其他資源
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969760"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="bc9b1-105">MrmResourceIndexerMessageSeverity 列舉</span><span class="sxs-lookup"><span data-stu-id="bc9b1-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="bc9b1-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc9b1-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bc9b1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc9b1-108">定義常數，指定資源索引子訊息的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="bc9b1-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9b1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc9b1-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="bc9b1-111">常數</span><span class="sxs-lookup"><span data-stu-id="bc9b1-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc9b1-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span><span class="sxs-lookup"><span data-stu-id="bc9b1-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b1-113">指出訊息是詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b1-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span><span class="sxs-lookup"><span data-stu-id="bc9b1-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b1-115">指出訊息為資訊。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b1-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span><span class="sxs-lookup"><span data-stu-id="bc9b1-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b1-117">指出訊息是警告。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b1-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span><span class="sxs-lookup"><span data-stu-id="bc9b1-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b1-119">指出訊息是錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc9b1-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc9b1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc9b1-120">Requirements</span></span>



| <span data-ttu-id="bc9b1-121">需求</span><span class="sxs-lookup"><span data-stu-id="bc9b1-121">Requirement</span></span> | <span data-ttu-id="bc9b1-122">值</span><span class="sxs-lookup"><span data-stu-id="bc9b1-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9b1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc9b1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9b1-124">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc9b1-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bc9b1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc9b1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9b1-126">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc9b1-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc9b1-127">標頭</span><span class="sxs-lookup"><span data-stu-id="bc9b1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc9b1-128"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc9b1-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc9b1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc9b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc9b1-130">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="bc9b1-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

