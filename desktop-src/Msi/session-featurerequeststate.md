---
description: FeatureRequestState 屬性是會話物件的讀寫屬性。
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: FeatureRequestState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981354"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="9f6b2-103">FeatureRequestState 屬性</span><span class="sxs-lookup"><span data-stu-id="9f6b2-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="9f6b2-104">**FeatureRequestState** 屬性是 [**會話**](session-object.md)物件的讀寫屬性。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="9f6b2-105">您可以使用它來取得功能的目前動作狀態，或要求功能及其子功能的動作變更。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="9f6b2-106">功能必須在 [功能](feature-table.md) 表中命名。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="9f6b2-107">如果要求某項功能的動作狀態變更，則變更功能之所有元件的動作狀態也可能會變更。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="9f6b2-108">由多項功能所共用之元件的動作狀態，會根據新的功能動作狀態進行適當的變更 (請參閱備註) 。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="9f6b2-109">**FeatureRequestState** 屬性也可以藉由指定關鍵字 all （而非特定功能名稱）來一次設定所有功能。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="9f6b2-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6b2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f6b2-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="9f6b2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9f6b2-112">Property value</span></span>

<span data-ttu-id="9f6b2-113">必要的字串，指定要設定之功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="9f6b2-114">若要將所有功能設定為所需的要求狀態，請使用保留的不區分大小寫單字：全部。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f6b2-115">備註</span><span class="sxs-lookup"><span data-stu-id="9f6b2-115">Remarks</span></span>

<span data-ttu-id="9f6b2-116">呼叫 **FeatureRequestState** 之前，必須先呼叫 [**SetInstallLevel**](session-setinstalllevel.md)方法。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="9f6b2-117">如果目前正在要求此功能的狀態， **FeatureRequestState** 屬性會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="9f6b2-118">選取狀態名稱</span><span class="sxs-lookup"><span data-stu-id="9f6b2-118">Selection state name</span></span>         | <span data-ttu-id="9f6b2-119">意義</span><span class="sxs-lookup"><span data-stu-id="9f6b2-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9f6b2-120">msiInstallStateUnknown =-1</span><span class="sxs-lookup"><span data-stu-id="9f6b2-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="9f6b2-121">這項功能不會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-121">No action is taken for the feature.</span></span> <span data-ttu-id="9f6b2-122">這相當於 null。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="9f6b2-123">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="9f6b2-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="9f6b2-124">即將公告功能。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="9f6b2-125">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="9f6b2-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="9f6b2-126">即將移除功能。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="9f6b2-127">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="9f6b2-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="9f6b2-128">功能會安裝為執行本機。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="9f6b2-129">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="9f6b2-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="9f6b2-130">功能是以執行來源的形式安裝。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="9f6b2-131">msiInstallStateDefault = 5</span><span class="sxs-lookup"><span data-stu-id="9f6b2-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="9f6b2-132">功能是以功能目前的動作狀態重新安裝。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="9f6b2-133">例如，下列程式會從 VBScript 自訂動作取得 "MyFeature" 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="9f6b2-134">如果正在設定功能的狀態， **FeatureRequestState** 屬性應該設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="9f6b2-135">選取狀態名稱</span><span class="sxs-lookup"><span data-stu-id="9f6b2-135">Selection state name</span></span>          | <span data-ttu-id="9f6b2-136">意義</span><span class="sxs-lookup"><span data-stu-id="9f6b2-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="9f6b2-137">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="9f6b2-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="9f6b2-138">公告此功能。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="9f6b2-139">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="9f6b2-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="9f6b2-140">移除功能。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="9f6b2-141">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="9f6b2-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="9f6b2-142">將功能安裝為執行本機。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="9f6b2-143">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="9f6b2-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="9f6b2-144">將功能安裝為從原始碼執行。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="9f6b2-145">例如，下列來自 VBScript 自訂動作的要求，它會將 "MyFeature" 安裝為在電腦本機上執行。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="9f6b2-146">呼叫 **FeatureRequestState** 時，安裝程式會嘗試將系結至指定功能之每個元件的動作狀態，盡可能設定為最理想的狀態。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="9f6b2-147">不過，在一般情況下，要求無法完全遵守。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="9f6b2-148">例如，如果功能系結至兩個元件（元件 A 和元件 B），則透過 [FeatureComponents](featurecomponents-table.md) 資料表和元件 a 具有 **msidbComponentAttributesLocalOnly** 屬性，而元件 b 具有 **msidbComponentAttributesSourceOnly** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="9f6b2-149">在此情況下，如果呼叫 **FeatureRequestState** 時所要求的狀態為 MsiInstallStateLocal 或 msiInstallStateSource，則這兩個元件無法接受此要求。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="9f6b2-150">在此情況下，您可以將元件 A 設為 msiInstallStateLocal，並將元件 B 設定為 msiInstallStateSource，來開啟這兩個元件。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="9f6b2-151">如果有一個以上的功能連結至單一元件，則該元件的最終動作狀態會依照下列方式決定：如果至少有一個功能呼叫要在本機安裝元件，則會安裝 msiInstallStateLocal。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="9f6b2-152">如果至少有一個功能呼叫要從來源媒體執行元件，則會安裝 msiInstallStateSource。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="9f6b2-153">如果至少有一個功能呼叫移除元件，則動作狀態為 msiInstallStateAbsent。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="9f6b2-154">如需如何選取功能以進行安裝的詳細資訊，請參閱 [功能](feature-table.md) 表。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="9f6b2-155">如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6b2-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f6b2-156">Requirements</span></span>



| <span data-ttu-id="9f6b2-157">需求</span><span class="sxs-lookup"><span data-stu-id="9f6b2-157">Requirement</span></span> | <span data-ttu-id="9f6b2-158">值</span><span class="sxs-lookup"><span data-stu-id="9f6b2-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6b2-159">版本</span><span class="sxs-lookup"><span data-stu-id="9f6b2-159">Version</span></span><br/> | <span data-ttu-id="9f6b2-160">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9f6b2-161">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="9f6b2-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9f6b2-162">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9f6b2-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9f6b2-163">DLL</span><span class="sxs-lookup"><span data-stu-id="9f6b2-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="9f6b2-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f6b2-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9f6b2-165">IID</span><span class="sxs-lookup"><span data-stu-id="9f6b2-165">IID</span></span><br/>     | <span data-ttu-id="9f6b2-166">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9f6b2-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="9f6b2-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f6b2-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6b2-168">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="9f6b2-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="9f6b2-169">功能</span><span class="sxs-lookup"><span data-stu-id="9f6b2-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




