---
title: 'MrmDumpType 列舉 (MrmResourceIndexer) '
description: 定義常數，指定要產生的 PRI 檔案傾印類型。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- MrmDumpType 列舉功能表和其他資源
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465597"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="a6c98-105">MrmDumpType 列舉</span><span class="sxs-lookup"><span data-stu-id="a6c98-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="a6c98-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a6c98-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a6c98-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a6c98-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a6c98-108">定義常數，指定要產生的 PRI 檔案傾印類型。</span><span class="sxs-lookup"><span data-stu-id="a6c98-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="a6c98-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="a6c98-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6c98-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6c98-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="a6c98-111">常數</span><span class="sxs-lookup"><span data-stu-id="a6c98-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a6c98-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType \_ 基本**</span><span class="sxs-lookup"><span data-stu-id="a6c98-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="a6c98-113">指定傾印應該是基本的。</span><span class="sxs-lookup"><span data-stu-id="a6c98-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="a6c98-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType \_ 詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="a6c98-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="a6c98-115">指定應該詳細的傾印。</span><span class="sxs-lookup"><span data-stu-id="a6c98-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="a6c98-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="a6c98-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="a6c98-117">指定傾印應該是架構。</span><span class="sxs-lookup"><span data-stu-id="a6c98-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6c98-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6c98-118">Requirements</span></span>



| <span data-ttu-id="a6c98-119">需求</span><span class="sxs-lookup"><span data-stu-id="a6c98-119">Requirement</span></span> | <span data-ttu-id="a6c98-120">值</span><span class="sxs-lookup"><span data-stu-id="a6c98-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c98-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6c98-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c98-122">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6c98-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6c98-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6c98-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c98-124">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6c98-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6c98-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a6c98-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c98-126"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6c98-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6c98-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6c98-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c98-128">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="a6c98-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

