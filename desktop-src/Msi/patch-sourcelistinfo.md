---
description: Patch 物件的 SourceListInfo 屬性會取得並設定 patch 的來源資訊屬性。 這個屬性會呼叫 MsiSourceListGetInfo 或 MsiSourceListSetInfo。 這是讀取或寫入屬性。
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: SourceListInfo 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994620"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="f924b-105">SourceListInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="f924b-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="f924b-106">[**Patch**](patch-object.md)物件的 **SourceListInfo** 屬性會取得並設定 patch 的來源資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="f924b-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="f924b-107">這個屬性會呼叫 [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) 或 [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)。</span><span class="sxs-lookup"><span data-stu-id="f924b-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="f924b-108">這是讀取或寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="f924b-108">This is a read or write property.</span></span>

<span data-ttu-id="f924b-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f924b-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f924b-110">語法</span><span class="sxs-lookup"><span data-stu-id="f924b-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="f924b-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="f924b-111">Property value</span></span>

<span data-ttu-id="f924b-112">要查詢或設定之修補程式的來源資訊屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="f924b-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="f924b-113">如需可能的值，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="f924b-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="f924b-114">備註</span><span class="sxs-lookup"><span data-stu-id="f924b-114">Remarks</span></span>

<span data-ttu-id="f924b-115">並非所有可抓取的屬性都可以設定。</span><span class="sxs-lookup"><span data-stu-id="f924b-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="f924b-116">*SzProperty* 參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f924b-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="f924b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="f924b-117">Property</span></span>         | <span data-ttu-id="f924b-118">可以設定嗎？</span><span class="sxs-lookup"><span data-stu-id="f924b-118">Can set?</span></span> | <span data-ttu-id="f924b-119">意義</span><span class="sxs-lookup"><span data-stu-id="f924b-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f924b-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="f924b-120">MediaPackagePath</span></span> | <span data-ttu-id="f924b-121">Y</span><span class="sxs-lookup"><span data-stu-id="f924b-121">Y</span></span>        | <span data-ttu-id="f924b-122">相對於安裝媒體根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="f924b-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="f924b-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="f924b-123">DiskPrompt</span></span>       | <span data-ttu-id="f924b-124">Y</span><span class="sxs-lookup"><span data-stu-id="f924b-124">Y</span></span>        | <span data-ttu-id="f924b-125">提示使用者輸入安裝媒體時所用的提示範本。</span><span class="sxs-lookup"><span data-stu-id="f924b-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="f924b-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="f924b-126">LastUsedSource</span></span>   | <span data-ttu-id="f924b-127">Y</span><span class="sxs-lookup"><span data-stu-id="f924b-127">Y</span></span>        | <span data-ttu-id="f924b-128">修補程式最近使用的來源位置。</span><span class="sxs-lookup"><span data-stu-id="f924b-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="f924b-129">當您設定這個屬性時，請在來源位置前面加上網路來源的 "n;"，或輸入 "u;" 作為 URL 類型。</span><span class="sxs-lookup"><span data-stu-id="f924b-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="f924b-130">例如，使用 "n; \\ \\臨時 \\ \\ 測試 "或" u; https://microsoft.com/Patches/Office/SP1 "。</span><span class="sxs-lookup"><span data-stu-id="f924b-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="f924b-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="f924b-131">LastUsedType</span></span>     | <span data-ttu-id="f924b-132">N</span><span class="sxs-lookup"><span data-stu-id="f924b-132">N</span></span>        | <span data-ttu-id="f924b-133">如果最後使用的來源是網路位置，則為 "n"。</span><span class="sxs-lookup"><span data-stu-id="f924b-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="f924b-134">如果最後使用的來源是 URL 位置，則為 "u"。</span><span class="sxs-lookup"><span data-stu-id="f924b-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="f924b-135">如果最後使用的來源是媒體，則為 "m"。</span><span class="sxs-lookup"><span data-stu-id="f924b-135">"m" if the last used source was media.</span></span> <span data-ttu-id="f924b-136">空字串 ( "" ) 如果沒有最後使用的來源。</span><span class="sxs-lookup"><span data-stu-id="f924b-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="f924b-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="f924b-137">PackageName</span></span>      | <span data-ttu-id="f924b-138">Y</span><span class="sxs-lookup"><span data-stu-id="f924b-138">Y</span></span>        | <span data-ttu-id="f924b-139">來源上 Windows Installer 封裝或修補封裝的名稱。</span><span class="sxs-lookup"><span data-stu-id="f924b-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f924b-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="f924b-140">Requirements</span></span>



| <span data-ttu-id="f924b-141">需求</span><span class="sxs-lookup"><span data-stu-id="f924b-141">Requirement</span></span> | <span data-ttu-id="f924b-142">值</span><span class="sxs-lookup"><span data-stu-id="f924b-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f924b-143">版本</span><span class="sxs-lookup"><span data-stu-id="f924b-143">Version</span></span><br/> | <span data-ttu-id="f924b-144">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="f924b-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f924b-145">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="f924b-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f924b-146">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f924b-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f924b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f924b-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="f924b-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f924b-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f924b-149">IID</span><span class="sxs-lookup"><span data-stu-id="f924b-149">IID</span></span><br/>     | <span data-ttu-id="f924b-150">IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f924b-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="f924b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f924b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f924b-152">**Patch**</span><span class="sxs-lookup"><span data-stu-id="f924b-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="f924b-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f924b-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="f924b-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="f924b-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="f924b-155">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="f924b-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




