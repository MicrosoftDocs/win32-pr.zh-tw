---
title: 'MrmPlatformVersion 列舉 (MrmResourceIndexer) '
description: 定義指定平臺版本的常數。 如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱封裝資源索引 (PRI) Api 和自訂群組建系統。
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- MrmPlatformVersion 列舉功能表和其他資源
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935019"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="99908-105">MrmPlatformVersion 列舉</span><span class="sxs-lookup"><span data-stu-id="99908-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="99908-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="99908-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="99908-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="99908-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="99908-108">定義指定平臺版本的常數。</span><span class="sxs-lookup"><span data-stu-id="99908-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="99908-109">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="99908-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="99908-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="99908-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="99908-111">常數</span><span class="sxs-lookup"><span data-stu-id="99908-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="99908-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="99908-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="99908-113">指定平臺版本是預設值。</span><span class="sxs-lookup"><span data-stu-id="99908-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="99908-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="99908-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="99908-115">指定 Windows 10.0.0.0 的平臺版本。</span><span class="sxs-lookup"><span data-stu-id="99908-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="99908-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="99908-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="99908-117">指定 Windows 10.0.0.5 的平臺版本。</span><span class="sxs-lookup"><span data-stu-id="99908-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99908-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="99908-118">Requirements</span></span>



| <span data-ttu-id="99908-119">需求</span><span class="sxs-lookup"><span data-stu-id="99908-119">Requirement</span></span> | <span data-ttu-id="99908-120">值</span><span class="sxs-lookup"><span data-stu-id="99908-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99908-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99908-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99908-122">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99908-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="99908-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99908-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99908-124">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99908-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="99908-125">標頭</span><span class="sxs-lookup"><span data-stu-id="99908-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="99908-126"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="99908-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99908-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99908-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99908-128">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="99908-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

