---
description: 安裝程式物件的 UILevel 屬性是讀寫屬性，它會指出在目前的進程空間內開啟和處理後續封裝時，所要使用的使用者介面型別。
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: UILevel 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999723"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="ba646-103">UILevel 屬性</span><span class="sxs-lookup"><span data-stu-id="ba646-103">Installer.UILevel property</span></span>

<span data-ttu-id="ba646-104">[**安裝程式**](installer-object.md)物件的 **UILevel** 屬性是讀寫屬性，它會指出在目前的進程空間內開啟和處理後續封裝時，所要使用的使用者介面型別。</span><span class="sxs-lookup"><span data-stu-id="ba646-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="ba646-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba646-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba646-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba646-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="ba646-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="ba646-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ba646-108">備註</span><span class="sxs-lookup"><span data-stu-id="ba646-108">Remarks</span></span>



| <span data-ttu-id="ba646-109">使用者介面層級</span><span class="sxs-lookup"><span data-stu-id="ba646-109">User interface level</span></span>   | <span data-ttu-id="ba646-110">值</span><span class="sxs-lookup"><span data-stu-id="ba646-110">Value</span></span> | <span data-ttu-id="ba646-111">描述</span><span class="sxs-lookup"><span data-stu-id="ba646-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba646-112">msiUILevelNoChange</span><span class="sxs-lookup"><span data-stu-id="ba646-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="ba646-113">0</span><span class="sxs-lookup"><span data-stu-id="ba646-113">0</span></span>     | <span data-ttu-id="ba646-114">不會變更 UI 層級。</span><span class="sxs-lookup"><span data-stu-id="ba646-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ba646-115">msiUILevelDefault</span><span class="sxs-lookup"><span data-stu-id="ba646-115">msiUILevelDefault</span></span>      | <span data-ttu-id="ba646-116">1</span><span class="sxs-lookup"><span data-stu-id="ba646-116">1</span></span>     | <span data-ttu-id="ba646-117">使用預設的 UI 層級。</span><span class="sxs-lookup"><span data-stu-id="ba646-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="ba646-118">msiUILevelNone</span><span class="sxs-lookup"><span data-stu-id="ba646-118">msiUILevelNone</span></span>         | <span data-ttu-id="ba646-119">2</span><span class="sxs-lookup"><span data-stu-id="ba646-119">2</span></span>     | <span data-ttu-id="ba646-120">無訊息安裝。</span><span class="sxs-lookup"><span data-stu-id="ba646-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="ba646-121">msiUILevelBasic</span><span class="sxs-lookup"><span data-stu-id="ba646-121">msiUILevelBasic</span></span>        | <span data-ttu-id="ba646-122">3</span><span class="sxs-lookup"><span data-stu-id="ba646-122">3</span></span>     | <span data-ttu-id="ba646-123">簡單的進度和錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="ba646-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="ba646-124">msiUILevelReduced</span><span class="sxs-lookup"><span data-stu-id="ba646-124">msiUILevelReduced</span></span>      | <span data-ttu-id="ba646-125">4</span><span class="sxs-lookup"><span data-stu-id="ba646-125">4</span></span>     | <span data-ttu-id="ba646-126">已隱藏撰寫的 UI 和 wizard 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ba646-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="ba646-127">msiUILevelFull</span><span class="sxs-lookup"><span data-stu-id="ba646-127">msiUILevelFull</span></span>         | <span data-ttu-id="ba646-128">5</span><span class="sxs-lookup"><span data-stu-id="ba646-128">5</span></span>     | <span data-ttu-id="ba646-129">使用嚮導、進度和錯誤撰寫的 UI。</span><span class="sxs-lookup"><span data-stu-id="ba646-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="ba646-130">msiUILevelHideCancel</span><span class="sxs-lookup"><span data-stu-id="ba646-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="ba646-131">32</span><span class="sxs-lookup"><span data-stu-id="ba646-131">32</span></span>    | <span data-ttu-id="ba646-132">如果與 msiUILevelBasic 值結合，安裝程式會顯示進度對話方塊，但不會在對話方塊中顯示 [ **取消** ] 按鈕，以防止使用者取消安裝。</span><span class="sxs-lookup"><span data-stu-id="ba646-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="ba646-133">msiUILevelProgressOnly</span><span class="sxs-lookup"><span data-stu-id="ba646-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="ba646-134">64</span><span class="sxs-lookup"><span data-stu-id="ba646-134">64</span></span>    | <span data-ttu-id="ba646-135">如果與 msiUILevelBasic 值結合，安裝程式會顯示進度對話方塊，但不會顯示任何強制回應對話方塊或錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ba646-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="ba646-136">msiUILevelEndDialog</span><span class="sxs-lookup"><span data-stu-id="ba646-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="ba646-137">128</span><span class="sxs-lookup"><span data-stu-id="ba646-137">128</span></span>   | <span data-ttu-id="ba646-138">如果與上述任何值結合，安裝程式會在安裝成功或發生錯誤時，顯示模式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ba646-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="ba646-139">如果使用者取消，則不會顯示任何對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ba646-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="ba646-140">另請參閱， [從自訂動作判斷 UI 層級](determining-ui-level-from-a-custom-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ba646-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba646-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba646-141">Requirements</span></span>



| <span data-ttu-id="ba646-142">需求</span><span class="sxs-lookup"><span data-stu-id="ba646-142">Requirement</span></span> | <span data-ttu-id="ba646-143">值</span><span class="sxs-lookup"><span data-stu-id="ba646-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba646-144">版本</span><span class="sxs-lookup"><span data-stu-id="ba646-144">Version</span></span><br/> | <span data-ttu-id="ba646-145">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ba646-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ba646-146">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ba646-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ba646-147">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ba646-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ba646-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ba646-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba646-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba646-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ba646-150">IID</span><span class="sxs-lookup"><span data-stu-id="ba646-150">IID</span></span><br/>     | <span data-ttu-id="ba646-151">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ba646-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




