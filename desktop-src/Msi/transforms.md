---
description: '[轉換] 屬性是安裝套件時，安裝程式所套用的轉換清單。'
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: 轉換屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abbb45db507f7ab813b96e9023634cbe217b554
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976181"
---
# <a name="transforms-property"></a><span data-ttu-id="e130b-103">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="e130b-103">TRANSFORMS property</span></span>

<span data-ttu-id="e130b-104">[ **轉換** ] 屬性是安裝套件時，安裝程式所套用的轉換清單。</span><span class="sxs-lookup"><span data-stu-id="e130b-104">The **TRANSFORMS** property is a list of the transforms that the installer applies when installing the package.</span></span> <span data-ttu-id="e130b-105">安裝程式會依照它們在屬性中所列的順序來套用轉換。</span><span class="sxs-lookup"><span data-stu-id="e130b-105">The installer applies the transforms in the same order as they are listed in the property.</span></span> <span data-ttu-id="e130b-106">轉換可以依其檔案名或完整路徑來指定。</span><span class="sxs-lookup"><span data-stu-id="e130b-106">Transforms can be specified by their filename or full path.</span></span> <span data-ttu-id="e130b-107">若要指定多個轉換，請以分號分隔每個檔案名或完整路徑 (; ) 。</span><span class="sxs-lookup"><span data-stu-id="e130b-107">To specify multiple transforms, separate each file name or full path with a semicolon (;).</span></span> <span data-ttu-id="e130b-108">例如，若要將三個轉換套用至封裝，請將 **轉換** 設定為檔案名清單或完整路徑清單。</span><span class="sxs-lookup"><span data-stu-id="e130b-108">For example, to apply three transforms to a package, set **TRANSFORMS** to a list of file names or to a list of full paths.</span></span>

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

<span data-ttu-id="e130b-109">您可以指定將轉換檔案內嵌在 .msi 檔案的儲存體中，而不是獨立的檔案，方法是在檔案名前面加上冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="e130b-109">You can indicate that a transform file is embedded in a storage of the .msi file, rather than as a stand-alone file, by prefixing the filename with a colon (:).</span></span> <span data-ttu-id="e130b-110">例如，下列範例表示 transform1 和 transform2 都內嵌在 .msi 檔案中，而 transform3 則是獨立的檔案。</span><span class="sxs-lookup"><span data-stu-id="e130b-110">For example, the following example indicates that transform1.mst and transform2.mst are embedded inside the .msi file and that transform3.mst is a stand-alone file.</span></span>

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

<span data-ttu-id="e130b-111">安裝程式需要在每次安裝、公告、隨選安裝或封裝的維護 **安裝中所** 列的轉換。</span><span class="sxs-lookup"><span data-stu-id="e130b-111">The installer requires the transforms listed in **TRANSFORMS** at every installation, advertisement, installation-on-demand, or maintenance installation of the package.</span></span> <span data-ttu-id="e130b-112">[TransformsSecure 原則](transformssecure-policy.md)原則、**轉換** 屬性和 **轉換** 字串的第一個字元會通知安裝程式如何處理獨立轉換檔案的來源復原。</span><span class="sxs-lookup"><span data-stu-id="e130b-112">The [TransformsSecure policy](transformssecure-policy.md) policy, the **TRANSFORMS** property, and the first character of the **TRANSFORMS** string informs the installer how to handle the source resiliency of stand-alone transform files.</span></span> <span data-ttu-id="e130b-113">Windows Installer 會將設定 [TransformsAtSource 原則](transformsatsource-policy.md) 或 [**TransformsAtSource**](transformsatsource.md) 視為與 TransformsSecure 原則和 [**TransformsSecure**](transformssecure.md)相同。</span><span class="sxs-lookup"><span data-stu-id="e130b-113">Windows Installer treats setting [TransformsAtSource policy](transformsatsource-policy.md) or [**TRANSFORMSATSOURCE**](transformsatsource.md) the same as TransformsSecure policy and [**TRANSFORMSSECURE**](transformssecure.md).</span></span> <span data-ttu-id="e130b-114">請注意，內嵌在 .msi 檔案中的轉換並不會被快取，而且一律會從封裝中取得。</span><span class="sxs-lookup"><span data-stu-id="e130b-114">Note that transforms embedded in the .msi file are not cached and are always obtained from the package.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e130b-115">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="e130b-115">TRANSFORMS Property</span></span></th>
<th><span data-ttu-id="e130b-116">安全轉換</span><span class="sxs-lookup"><span data-stu-id="e130b-116">Transforms Secure</span></span></th>
<th><span data-ttu-id="e130b-117">快取和復原</span><span class="sxs-lookup"><span data-stu-id="e130b-117">Caching and Resiliency</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e130b-118">@ [<em>檔案名的清單</em>] 範例：</span><span class="sxs-lookup"><span data-stu-id="e130b-118">@[<em>list of filenames</em>] Example:</span></span><br/> <span data-ttu-id="e130b-119">@transform1.mst; transform2 .mst;transform3 .mst</span><span class="sxs-lookup"><span data-stu-id="e130b-119">@transform1.mst;transform2.mst; transform3.mst</span></span><br/></td>
<td><span data-ttu-id="e130b-120">沒有影響。</span><span class="sxs-lookup"><span data-stu-id="e130b-120">No effect.</span></span></td>
<td><span data-ttu-id="e130b-121"><a href="secure-at-source-transforms.md">安全來源轉換</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-121"><a href="secure-at-source-transforms.md">Secure-At-Source transforms</a>.</span></span> <span data-ttu-id="e130b-122">轉換的來源必須位於封裝來源的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="e130b-122">The source of the transforms must be at the root of the source for the package.</span></span> <span data-ttu-id="e130b-123">安裝或公告封裝時，安裝程式會將使用者電腦上的轉換儲存在使用者沒有寫入存取權的快取中。</span><span class="sxs-lookup"><span data-stu-id="e130b-123">When the package is installed or advertised, the installer saves the transforms on the user's computer in a cache where the user does not have write access.</span></span> <span data-ttu-id="e130b-124">如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。</span><span class="sxs-lookup"><span data-stu-id="e130b-124">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="e130b-125">方法與搜尋 .msi 檔案的來源清單相同。</span><span class="sxs-lookup"><span data-stu-id="e130b-125">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="e130b-126">請參閱 <a href="source-resiliency.md">來源復原</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-126">See <a href="source-resiliency.md">Source Resiliency</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e130b-127">|[<em>路徑清單</em>]例子：</span><span class="sxs-lookup"><span data-stu-id="e130b-127">|[<em>list of paths</em>] Example:</span></span><br/>
<pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst</code></pre></td>
<td><span data-ttu-id="e130b-128">沒有影響。</span><span class="sxs-lookup"><span data-stu-id="e130b-128">No effect.</span></span></td>
<td><span data-ttu-id="e130b-129"><a href="secure-full-path-transforms.md">安全-完整路徑轉換</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-129"><a href="secure-full-path-transforms.md">Secure-Full-Path transforms</a>.</span></span> <span data-ttu-id="e130b-130">每個轉換的來源都必須在傳遞至 <strong>轉換</strong>的完整路徑上。</span><span class="sxs-lookup"><span data-stu-id="e130b-130">The source of each transform must be at the full path passed to <strong>TRANSFORMS</strong>.</span></span> <span data-ttu-id="e130b-131">轉換來源不一定要位於封裝的來源。</span><span class="sxs-lookup"><span data-stu-id="e130b-131">The transform source does not have to be located at the source of the package.</span></span> <span data-ttu-id="e130b-132">安裝或公告封裝時，安裝程式會將使用者電腦上的轉換儲存在使用者沒有寫入存取權的快取中。</span><span class="sxs-lookup"><span data-stu-id="e130b-132">When the package is installed or advertised, the installer saves the transforms on the user's computer in a cache where the user does not have write access.</span></span> <span data-ttu-id="e130b-133">如果轉換的本機複本無法使用，安裝程式只能從指定路徑的來源還原快取。</span><span class="sxs-lookup"><span data-stu-id="e130b-133">If the local copy of the transform becomes unavailable the installer can only restore the cache from the source at the specified path.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e130b-134">[<em>檔案名清單</em>]第一個字元不是 @ 或 |。</span><span class="sxs-lookup"><span data-stu-id="e130b-134">[<em>list of filenames</em>] The first character is not @ or |.</span></span><br/> <span data-ttu-id="e130b-135">範例：</span><span class="sxs-lookup"><span data-stu-id="e130b-135">Example:</span></span><br/> <span data-ttu-id="e130b-136">transform1 .mst; transform2 .mst;transform3 .mst</span><span class="sxs-lookup"><span data-stu-id="e130b-136">transform1.mst;transform2.mst; transform3.mst</span></span><br/></td>
<td><span data-ttu-id="e130b-137"><a href="transformssecure-policy.md">TransformsSecure 原則</a> 或 <a href="transformssecure.md"><strong>TransformsSecure</strong></a> 設定為1或</span><span class="sxs-lookup"><span data-stu-id="e130b-137"><a href="transformssecure-policy.md">TransformsSecure policy</a> or <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> set to 1 OR</span></span><br/> <span data-ttu-id="e130b-138"><a href="transformsatsource-policy.md">TransformsAtSource 原則</a> 或 <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> 設定為1。</span><span class="sxs-lookup"><span data-stu-id="e130b-138"><a href="transformsatsource-policy.md">TransformsAtSource policy</a> or <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> set to 1.</span></span><br/></td>
<td><span data-ttu-id="e130b-139">如果 <strong>轉換</strong> 是檔案名的清單，則安裝程式會將它們視為 <a href="secure-at-source-transforms.md">安全來源的轉換</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-139">If <strong>TRANSFORMS</strong> is a list of filenames, the installer treats them as <a href="secure-at-source-transforms.md">Secure-At-Source transforms</a>.</span></span> <span data-ttu-id="e130b-140">如果 <strong>轉換</strong> 是完整路徑的清單，則安裝程式會將它們視為 <a href="secure-full-path-transforms.md">安全的完整路徑轉換</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-140">If <strong>TRANSFORMS</strong> is a list of full paths, the installer treats them as <a href="secure-full-path-transforms.md">Secure-Full-Path transforms</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e130b-141">[<em>檔案名清單</em>]第一個字元不是 @ 或 |。</span><span class="sxs-lookup"><span data-stu-id="e130b-141">[<em>list of filenames</em>] The first character is not @ or |.</span></span><br/> <span data-ttu-id="e130b-142">範例：</span><span class="sxs-lookup"><span data-stu-id="e130b-142">Example:</span></span><br/> <span data-ttu-id="e130b-143">transform1 .mst; transform2 .mst;transform3 .mst</span><span class="sxs-lookup"><span data-stu-id="e130b-143">transform1.mst;transform2.mst; transform3.mst</span></span><br/></td>
<td><span data-ttu-id="e130b-144">未設定<a href="transformssecure-policy.md">TransformsSecure 原則</a>和<a href="transformssecure.md"><strong>TransformsSecure</strong></a></span><span class="sxs-lookup"><span data-stu-id="e130b-144"><a href="transformssecure-policy.md">TransformsSecure policy</a> and <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> are not set AND</span></span><br/> <span data-ttu-id="e130b-145">未設定<a href="transformsatsource-policy.md">TransformsAtSource 原則</a>和<a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="e130b-145"><a href="transformsatsource-policy.md">TransformsAtSource policy</a> and <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> are not set.</span></span><br/></td>
<td><span data-ttu-id="e130b-146">不<a href="unsecured-transforms.md">安全的轉換</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-146"><a href="unsecured-transforms.md">Unsecured Transforms</a>.</span></span> <span data-ttu-id="e130b-147">轉換的來源必須位於封裝來源的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="e130b-147">The source of the transforms must be at the root of the source for the package.</span></span> <span data-ttu-id="e130b-148">當封裝已安裝或公告每位使用者時，安裝程式會將轉換儲存在使用者的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="e130b-148">When the package is installed or advertised per-user, the installer saves the transforms in the user's profile.</span></span> <span data-ttu-id="e130b-149">這可讓使用者在電腦之間漫遊，同時維持其自訂。</span><span class="sxs-lookup"><span data-stu-id="e130b-149">This enables a user to roam between computers while maintaining their customizations.</span></span> <span data-ttu-id="e130b-150">針對每部電腦安裝，轉換會儲存在%windir%\Installer 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e130b-150">For a per-machine install, the transform is saved in the %windir%\Installer folder.</span></span> <span data-ttu-id="e130b-151">如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。</span><span class="sxs-lookup"><span data-stu-id="e130b-151">If the local copy of the transform becomes unavailable the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="e130b-152">方法與搜尋 .msi 檔案的來源清單相同。</span><span class="sxs-lookup"><span data-stu-id="e130b-152">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="e130b-153">請參閱 <a href="source-resiliency.md">來源復原</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-153">See <a href="source-resiliency.md">Source Resiliency</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e130b-154">[<em>路徑清單</em>]第一個字元不是 @ 或 |。</span><span class="sxs-lookup"><span data-stu-id="e130b-154">[<em>list of paths</em>] The first character is not @ or |.</span></span><br/> <span data-ttu-id="e130b-155">範例：</span><span class="sxs-lookup"><span data-stu-id="e130b-155">Example:</span></span><br/>
<pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre></td>
<td><span data-ttu-id="e130b-156">未設定<a href="transformsatsource-policy.md">TransformsAtSource 原則</a>和<a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e130b-156"><a href="transformsatsource-policy.md">TransformsAtSource policy</a> and <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> are not set AND</span></span><br/> <span data-ttu-id="e130b-157">未設定<a href="transformsatsource-policy.md">TransformsAtSource 原則</a>和<a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="e130b-157"><a href="transformsatsource-policy.md">TransformsAtSource policy</a> and <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> are not set..</span></span><br/></td>
<td><span data-ttu-id="e130b-158">不<a href="unsecured-transforms.md">安全的轉換</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-158"><a href="unsecured-transforms.md">Unsecured Transforms</a>.</span></span> <span data-ttu-id="e130b-159">當封裝已安裝或公告每位使用者時，安裝程式會將轉換儲存在使用者的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="e130b-159">When the package is installed or advertised per-user, the installer saves the transforms in the user's profile.</span></span> <span data-ttu-id="e130b-160">這可讓使用者在電腦之間漫遊，同時維持其自訂。</span><span class="sxs-lookup"><span data-stu-id="e130b-160">This enables a user to roam between computers while maintaining their customizations.</span></span> <span data-ttu-id="e130b-161">針對每部電腦安裝，轉換會儲存在%windir%\Installer 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e130b-161">For a per-machine install, the transform is saved in the %windir%\Installer folder.</span></span> <span data-ttu-id="e130b-162">如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。</span><span class="sxs-lookup"><span data-stu-id="e130b-162">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="e130b-163">方法與搜尋 .msi 檔案的來源清單相同。</span><span class="sxs-lookup"><span data-stu-id="e130b-163">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="e130b-164">請參閱 <a href="source-resiliency.md">來源復原</a>。</span><span class="sxs-lookup"><span data-stu-id="e130b-164">See <a href="source-resiliency.md">Source Resiliency</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e130b-165">您無法在相同的 **轉換** 清單中同時使用檔案名和路徑。</span><span class="sxs-lookup"><span data-stu-id="e130b-165">You cannot use filenames and paths together in the same **TRANSFORMS** list.</span></span> <span data-ttu-id="e130b-166">您無法在相同清單中同時指定安全和設定檔轉換。</span><span class="sxs-lookup"><span data-stu-id="e130b-166">You cannot specify secure and profile transforms together in the same list.</span></span> <span data-ttu-id="e130b-167">您可以將內嵌在套件中的轉換包含在具有其他轉換的清單中。</span><span class="sxs-lookup"><span data-stu-id="e130b-167">You may include transforms embedded in the package in a list with other transforms.</span></span>

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

<span data-ttu-id="e130b-168">請注意，因為轉換的清單分隔符號是分號字元，所以不能在轉換檔案名或路徑中使用分號。</span><span class="sxs-lookup"><span data-stu-id="e130b-168">Note that because the list delimiter for transforms is the semicolon character, semicolons must not be used in a transform filename or path.</span></span>

## <a name="remarks"></a><span data-ttu-id="e130b-169">備註</span><span class="sxs-lookup"><span data-stu-id="e130b-169">Remarks</span></span>

<span data-ttu-id="e130b-170">在使用 Windows Installer 設定 [TransformsSecure 原則](transformssecure-policy.md) 或 [**TransformsSecure**](transformssecure.md) 屬性的情況下， \| 使用命令列設定 **轉換** 時，不需要傳遞 @ 或符號。</span><span class="sxs-lookup"><span data-stu-id="e130b-170">In cases where the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property has been set with Windows Installer, it is not necessary to pass the @ or \| symbol when setting **TRANSFORMS** using the command line.</span></span> <span data-ttu-id="e130b-171">如果清單完全是由位於來源的檔案名所組成，或者完全是由完整路徑所組成，則安裝程式會採用安全來源或安全的-完整路徑。</span><span class="sxs-lookup"><span data-stu-id="e130b-171">The installer assumes Secure-At-Source or Secure-Full-Path if the list consists entirely of file names located at the source or consists entirely of full paths.</span></span> <span data-ttu-id="e130b-172">您仍然無法混用這兩種類型的轉換來源。</span><span class="sxs-lookup"><span data-stu-id="e130b-172">You still cannot mix the two types of transform sources.</span></span>

<span data-ttu-id="e130b-173">請注意，安裝程式會針對在第一次和維護安裝期間套用的不安全轉換使用不同的搜尋順序。</span><span class="sxs-lookup"><span data-stu-id="e130b-173">Note that the installer uses a different search order for unsecured transforms applied during first time and maintenance installations.</span></span> <span data-ttu-id="e130b-174">如需詳細資訊，請參閱不 [安全的轉換](unsecured-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="e130b-174">For more information, see [Unsecured Transforms](unsecured-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e130b-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="e130b-175">Requirements</span></span>



| <span data-ttu-id="e130b-176">需求</span><span class="sxs-lookup"><span data-stu-id="e130b-176">Requirement</span></span> | <span data-ttu-id="e130b-177">值</span><span class="sxs-lookup"><span data-stu-id="e130b-177">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e130b-178">版本</span><span class="sxs-lookup"><span data-stu-id="e130b-178">Version</span></span><br/> | <span data-ttu-id="e130b-179">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e130b-179">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e130b-180">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e130b-180">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e130b-181">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="e130b-181">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e130b-182">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="e130b-182">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e130b-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e130b-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e130b-184">屬性</span><span class="sxs-lookup"><span data-stu-id="e130b-184">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="e130b-185">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="e130b-185">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="e130b-186">合併和轉換</span><span class="sxs-lookup"><span data-stu-id="e130b-186">Merges and Transforms</span></span>](merges-and-transforms.md)
</dt> <dt>

[<span data-ttu-id="e130b-187">來源復原</span><span class="sxs-lookup"><span data-stu-id="e130b-187">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




