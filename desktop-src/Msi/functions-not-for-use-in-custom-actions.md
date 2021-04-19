---
description: 您永遠都不能從自訂動作呼叫下列資料庫函數。
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: 未在自訂動作中使用的函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c77c4714ca65614200cf77d6b207b6eebcaf179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978020"
---
# <a name="functions-not-for-use-in-custom-actions"></a><span data-ttu-id="11650-103">未在自訂動作中使用的函數</span><span class="sxs-lookup"><span data-stu-id="11650-103">Functions Not for Use in Custom Actions</span></span>

<span data-ttu-id="11650-104">您永遠都不能從自訂動作呼叫下列 [資料庫函數](database-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="11650-104">The following [Database Functions](database-functions.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="11650-105">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="11650-105">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="11650-106">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="11650-106">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="11650-107">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="11650-107">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [<span data-ttu-id="11650-108">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="11650-108">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [<span data-ttu-id="11650-109">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="11650-109">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [<span data-ttu-id="11650-110">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="11650-110">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [<span data-ttu-id="11650-111">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="11650-111">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [<span data-ttu-id="11650-112">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="11650-112">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [<span data-ttu-id="11650-113">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="11650-113">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [<span data-ttu-id="11650-114">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="11650-114">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="11650-115">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="11650-115">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [<span data-ttu-id="11650-116">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="11650-116">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [<span data-ttu-id="11650-117">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="11650-117">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [<span data-ttu-id="11650-118">**MsiPreviewBillboard**</span><span class="sxs-lookup"><span data-stu-id="11650-118">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [<span data-ttu-id="11650-119">**MsiPreviewDialog**</span><span class="sxs-lookup"><span data-stu-id="11650-119">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [<span data-ttu-id="11650-120">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="11650-120">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="11650-121">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="11650-121">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="11650-122">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="11650-122">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="11650-123">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="11650-123">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

<span data-ttu-id="11650-124">下列 [安裝程式函數](installer-function-reference.md) 永遠不能從自訂動作呼叫。</span><span class="sxs-lookup"><span data-stu-id="11650-124">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action.</span></span>

-   [<span data-ttu-id="11650-125">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="11650-125">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [<span data-ttu-id="11650-126">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="11650-126">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [<span data-ttu-id="11650-127">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="11650-127">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [<span data-ttu-id="11650-128">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="11650-128">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [<span data-ttu-id="11650-129">**MsiConfigureProductEx**</span><span class="sxs-lookup"><span data-stu-id="11650-129">**MsiConfigureProductEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [<span data-ttu-id="11650-130">**MsiEnableLog**</span><span class="sxs-lookup"><span data-stu-id="11650-130">**MsiEnableLog**</span></span>](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [<span data-ttu-id="11650-131">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="11650-131">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [<span data-ttu-id="11650-132">**MsiGetProductCode**</span><span class="sxs-lookup"><span data-stu-id="11650-132">**MsiGetProductCode**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [<span data-ttu-id="11650-133">**MsiGetProductProperty**</span><span class="sxs-lookup"><span data-stu-id="11650-133">**MsiGetProductProperty**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [<span data-ttu-id="11650-134">**MsiInstallMissingComponent**</span><span class="sxs-lookup"><span data-stu-id="11650-134">**MsiInstallMissingComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [<span data-ttu-id="11650-135">**MsiInstallMissingFile**</span><span class="sxs-lookup"><span data-stu-id="11650-135">**MsiInstallMissingFile**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [<span data-ttu-id="11650-136">**MsiInstallProduct**</span><span class="sxs-lookup"><span data-stu-id="11650-136">**MsiInstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [<span data-ttu-id="11650-137">**MsiOpenPackage**</span><span class="sxs-lookup"><span data-stu-id="11650-137">**MsiOpenPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [<span data-ttu-id="11650-138">**MsiOpenProduct**</span><span class="sxs-lookup"><span data-stu-id="11650-138">**MsiOpenProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [<span data-ttu-id="11650-139">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="11650-139">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [<span data-ttu-id="11650-140">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="11650-140">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [<span data-ttu-id="11650-141">**MsiSetExternalUI**</span><span class="sxs-lookup"><span data-stu-id="11650-141">**MsiSetExternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [<span data-ttu-id="11650-142">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="11650-142">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [<span data-ttu-id="11650-143">**MsiUseFeature**</span><span class="sxs-lookup"><span data-stu-id="11650-143">**MsiUseFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [<span data-ttu-id="11650-144">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="11650-144">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [<span data-ttu-id="11650-145">**MsiVerifyPackage**</span><span class="sxs-lookup"><span data-stu-id="11650-145">**MsiVerifyPackage**</span></span>](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

<span data-ttu-id="11650-146">如果這麼做會啟動另一個安裝，則永遠不會從自訂動作呼叫下列 [安裝程式](installer-function-reference.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="11650-146">The following [Installer Functions](installer-function-reference.md) must never be called from a custom action if doing so starts another installation.</span></span> <span data-ttu-id="11650-147">您可以從不會啟動另一個安裝的自訂動作來呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="11650-147">They may be called from a custom action that does not start another installation.</span></span>

-   [<span data-ttu-id="11650-148">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="11650-148">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [<span data-ttu-id="11650-149">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="11650-149">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [<span data-ttu-id="11650-150">**MsiProvideQualifiedComponentEx**</span><span class="sxs-lookup"><span data-stu-id="11650-150">**MsiProvideQualifiedComponentEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

<span data-ttu-id="11650-151">自訂動作永遠不應該產生新的執行緒，以使用 Windows Installer 函式來變更功能狀態、元件狀態，或從控制項事件傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="11650-151">A custom action should never spawn a new thread that uses Windows Installer functions to change the feature state, component state, or to send messages from a Control Event.</span></span> <span data-ttu-id="11650-152">嘗試這麼做會導致安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="11650-152">Attempting to do this causes the installation to fail.</span></span>

 

 



