---
title: '封裝常數 (AppModel. h) '
description: 指定如何處理封裝。
ms.assetid: 72E565C3-6CFD-47E3-8BAC-17D6E86B99DA
topic_type:
- apiref
api_name:
- PACKAGE_APPLICATIONS_MAX_COUNT
- PACKAGE_APPLICATIONS_MIN_COUNT
- PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES
- PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES
- PACKAGE_FILTER_ALL_LOADED
- PACKAGE_FILTER_BUNDLE
- PACKAGE_FILTER_DIRECT
- PACKAGE_FILTER_HEAD
- PACKAGE_FILTER_OPTIONAL
- PACKAGE_FILTER_RESOURCE
- PACKAGE_GRAPH_MAX_SIZE
- PACKAGE_GRAPH_MIN_SIZE
- PACKAGE_INFORMATION_BASIC
- PACKAGE_INFORMATION_FULL
- PACKAGE_MAX_DEPENDENCIES
- PACKAGE_MIN_DEPENDENCIES
- PACKAGE_PROPERTY_BUNDLE
- PACKAGE_PROPERTY_DEVELOPMENT_MODE
- PACKAGE_PROPERTY_FRAMEWORK
- PACKAGE_PROPERTY_OPTIONAL
- PACKAGE_PROPERTY_RESOURCE
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb3a4630eb6e132c7a82ea6b45839f6d2684cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967959"
---
# <a name="package-constants"></a><span data-ttu-id="b5d32-103">封裝常數</span><span class="sxs-lookup"><span data-stu-id="b5d32-103">Package constants</span></span>

<span data-ttu-id="b5d32-104">指定如何處理封裝。</span><span class="sxs-lookup"><span data-stu-id="b5d32-104">Specifies how packages are to be processed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b5d32-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="b5d32-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b5d32-106">Description</span><span class="sxs-lookup"><span data-stu-id="b5d32-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MAX_COUNT"></span><span id="package_applications_max_count"></span><dl> <span data-ttu-id="b5d32-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-108">封裝中應用程式的最大數目。</span><span class="sxs-lookup"><span data-stu-id="b5d32-108">The maximum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MIN_COUNT"></span><span id="package_applications_min_count"></span><dl> <span data-ttu-id="b5d32-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-110">封裝中應用程式的最小數目。</span><span class="sxs-lookup"><span data-stu-id="b5d32-110">The minimum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES"></span><span id="package_family_max_resource_packages"></span><dl> <span data-ttu-id="b5d32-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-112">封裝可擁有的資源套件數目上限。</span><span class="sxs-lookup"><span data-stu-id="b5d32-112">The maximum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES"></span><span id="package_family_min_resource_packages"></span><dl> <span data-ttu-id="b5d32-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-114">封裝可擁有的資源套件數目下限。</span><span class="sxs-lookup"><span data-stu-id="b5d32-114">The minimum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_ALL_LOADED"></span><span id="package_filter_all_loaded"></span><dl> <span data-ttu-id="b5d32-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-116">處理相依性圖形中的所有套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-116">Process all packages in the dependency graph.</span></span><br/> <span data-ttu-id="b5d32-117">這相當於<strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>。</span><span class="sxs-lookup"><span data-stu-id="b5d32-117">This is equivalent to <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span><br/>
<blockquote>
[!Note]<br /><span data-ttu-id="b5d32-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> 可能會在 Windows 8.1 之後變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b5d32-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="b5d32-119">相反地，請使用<strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>。</span><span class="sxs-lookup"><span data-stu-id="b5d32-119">Instead, use <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_BUNDLE"></span><span id="package_filter_bundle"></span><dl> <span data-ttu-id="b5d32-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-121">封裝圖形中的進程組合套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-121">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_DIRECT"></span><span id="package_filter_direct"></span><dl> <span data-ttu-id="b5d32-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-123">在相依性圖形中處理前端 (第一個) 套件的直接相依套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-123">Process the directly dependent packages of the head (first) package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_HEAD"></span><span id="package_filter_head"></span><dl> <span data-ttu-id="b5d32-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-125">處理相依性圖形中的第一個封裝。</span><span class="sxs-lookup"><span data-stu-id="b5d32-125">Process the first package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_OPTIONAL"></span><span id="package_filter_optional"></span><dl> <span data-ttu-id="b5d32-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-127">封裝圖形中的進程組合套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-127">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_RESOURCE"></span><span id="package_filter_resource"></span><dl> <span data-ttu-id="b5d32-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-129">處理套件圖形中的資源套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-129">Process resource packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MAX_SIZE"></span><span id="package_graph_max_size"></span><dl> <span data-ttu-id="b5d32-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt> (1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES) </dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-131">封裝圖形的大小上限。</span><span class="sxs-lookup"><span data-stu-id="b5d32-131">The maximum size of a package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MIN_SIZE"></span><span id="package_graph_min_size"></span><dl> <span data-ttu-id="b5d32-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-133">封裝圖形的大小下限。</span><span class="sxs-lookup"><span data-stu-id="b5d32-133">The minimum size of a package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_BASIC"></span><span id="package_information_basic"></span><dl> <span data-ttu-id="b5d32-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-135">取得基本資訊。</span><span class="sxs-lookup"><span data-stu-id="b5d32-135">Retrieve basic information.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_FULL"></span><span id="package_information_full"></span><dl> <span data-ttu-id="b5d32-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-137">取得完整資訊。</span><span class="sxs-lookup"><span data-stu-id="b5d32-137">Retrieve full information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_MAX_DEPENDENCIES"></span><span id="package_max_dependencies"></span><dl> <span data-ttu-id="b5d32-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-139">封裝相依的封裝數目上限。</span><span class="sxs-lookup"><span data-stu-id="b5d32-139">The maximum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_MIN_DEPENDENCIES"></span><span id="package_min_dependencies"></span><dl> <span data-ttu-id="b5d32-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-141">封裝相依的套件數目下限。</span><span class="sxs-lookup"><span data-stu-id="b5d32-141">The minimum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_BUNDLE"></span><span id="package_property_bundle"></span><dl> <span data-ttu-id="b5d32-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-143">封裝是套件組合套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-143">The package is a bundle package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_DEVELOPMENT_MODE"></span><span id="package_property_development_mode"></span><dl> <span data-ttu-id="b5d32-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-145">已向 <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>d</strong></a> 列舉註冊封裝。</span><span class="sxs-lookup"><span data-stu-id="b5d32-145">The package was registered with the <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>DeploymentOptions</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_FRAMEWORK"></span><span id="package_property_framework"></span><dl> <span data-ttu-id="b5d32-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-147">封裝是一個架構。</span><span class="sxs-lookup"><span data-stu-id="b5d32-147">The package is a framework.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_OPTIONAL"></span><span id="package_property_optional"></span><dl> <span data-ttu-id="b5d32-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-149">封裝是選用套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-149">The package is an optional package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_RESOURCE"></span><span id="package_property_resource"></span><dl> <span data-ttu-id="b5d32-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="b5d32-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b5d32-151">封裝是資源套件。</span><span class="sxs-lookup"><span data-stu-id="b5d32-151">The package is a resource package.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b5d32-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5d32-152">Requirements</span></span>



| <span data-ttu-id="b5d32-153">需求</span><span class="sxs-lookup"><span data-stu-id="b5d32-153">Requirement</span></span> | <span data-ttu-id="b5d32-154">值</span><span class="sxs-lookup"><span data-stu-id="b5d32-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d32-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5d32-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d32-156">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d32-156">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b5d32-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5d32-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d32-158">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5d32-158">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5d32-159">標頭</span><span class="sxs-lookup"><span data-stu-id="b5d32-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5d32-160"><dt>AppModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d32-160"><dt>AppModel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d32-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5d32-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d32-162">**GetCurrentPackageInfo**</span><span class="sxs-lookup"><span data-stu-id="b5d32-162">**GetCurrentPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)
</dt> <dt>

[<span data-ttu-id="b5d32-163">**GetPackageInfo**</span><span class="sxs-lookup"><span data-stu-id="b5d32-163">**GetPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)
</dt> <dt>

[<span data-ttu-id="b5d32-164">**PackageIdFromFullName**</span><span class="sxs-lookup"><span data-stu-id="b5d32-164">**PackageIdFromFullName**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)
</dt> </dl>

 

