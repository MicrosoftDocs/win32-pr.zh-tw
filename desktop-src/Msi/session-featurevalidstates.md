---
description: Session 物件的 FeatureValidStates 屬性會傳回代表位旗標的整數，其中每個相關位代表指定功能的有效安裝狀態。
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: FeatureValidStates 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991134"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="1fb0f-103">FeatureValidStates 屬性</span><span class="sxs-lookup"><span data-stu-id="1fb0f-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="1fb0f-104">[**Session**](session-object.md)物件的 **FeatureValidStates** 屬性會傳回代表位旗標的整數，其中每個相關位代表指定功能的有效安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="1fb0f-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb0f-106">語法</span><span class="sxs-lookup"><span data-stu-id="1fb0f-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="1fb0f-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="1fb0f-107">Property value</span></span>

<span data-ttu-id="1fb0f-108">要抓取其有效安裝狀態的功能專案所需的字串名稱。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fb0f-109">備註</span><span class="sxs-lookup"><span data-stu-id="1fb0f-109">Remarks</span></span>

<span data-ttu-id="1fb0f-110">傳回值是由位旗標所組成，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="1fb0f-111">位0：如果設定，則本機是有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="1fb0f-112">位1：如果設定，則來源是有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="1fb0f-113">只有在安裝程式呼叫 [CostInitialize](costinitialize-action.md)和 [CostFinalize](costfinalize-action.md)動作之後， **FeatureValidStates** 屬性才會成功。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="1fb0f-114">**FeatureValidStates** 會藉由查詢連結至指定功能的所有元件，而不考慮任何元件目前已安裝的狀態，來決定狀態有效性。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="1fb0f-115">功能可能有效的狀態如下所示：</span><span class="sxs-lookup"><span data-stu-id="1fb0f-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="1fb0f-116">如果功能不包含元件，則 INSTALLSTATE \_ 本機和 INSTALLSTATE \_ 來源都是功能的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="1fb0f-117">如果功能的至少一個元件具有 msidbComponentAttributesLocalOnly 或 msidbComponentAttributesOptional 的屬性，則 INSTALLSTATE \_ LOCAL 會是此功能的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="1fb0f-118">如果功能的至少一個元件具有 msidbComponentAttributesSourceOnly 或 msidbComponentAttributesOptional 的屬性，則 INSTALLSTATE \_ 來源會是此功能的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="1fb0f-119">如果屬於功能的元件檔案已修補或從壓縮的來源進行修補，則 INSTALLSTATE \_ 來源不會包含為功能的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="1fb0f-120">\_如果功能不允許公告 (msidbFeatureAttributesDisallowAdvertise) 或功能需要 (msidbFeatureAttributesNoUnsupportedAdvertise) 的平臺支援，而且平臺不支援它，則 INSTALLSTATE 公告不是有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="1fb0f-121">\_如果功能的屬性不包含 msidbFeatureAttributesUIDisallowAbsent，則 INSTALLSTATE 不會是此功能的有效狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="1fb0f-122">標示為遵循父功能的子功能的有效狀態 (msidbFeatureAttributesFollowParent) 是根據父功能的動作或已安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="1fb0f-123">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb0f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fb0f-124">Requirements</span></span>



| <span data-ttu-id="1fb0f-125">需求</span><span class="sxs-lookup"><span data-stu-id="1fb0f-125">Requirement</span></span> | <span data-ttu-id="1fb0f-126">值</span><span class="sxs-lookup"><span data-stu-id="1fb0f-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb0f-127">版本</span><span class="sxs-lookup"><span data-stu-id="1fb0f-127">Version</span></span><br/> | <span data-ttu-id="1fb0f-128">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1fb0f-129">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="1fb0f-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1fb0f-130">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1fb0f-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1fb0f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb0f-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="1fb0f-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fb0f-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1fb0f-133">IID</span><span class="sxs-lookup"><span data-stu-id="1fb0f-133">IID</span></span><br/>     | <span data-ttu-id="1fb0f-134">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1fb0f-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




