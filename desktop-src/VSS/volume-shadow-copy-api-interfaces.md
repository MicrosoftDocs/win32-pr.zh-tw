---
description: 磁碟區陰影複製服務 (VSS) API 都提供 COM 和 c + + 介面，以支援建立要求者和寫入器。
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: 磁片區陰影複製 API 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1291f0e63b18530f92d99f9d526202df078fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113188"
---
# <a name="volume-shadow-copy-api-interfaces"></a><span data-ttu-id="6fbc8-103">磁片區陰影複製 API 介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-103">Volume Shadow Copy API Interfaces</span></span>

<span data-ttu-id="6fbc8-104">磁碟區陰影複製服務 (VSS) API 都提供 COM 和 c + + 介面，以支援建立要求者和寫入器。</span><span class="sxs-lookup"><span data-stu-id="6fbc8-104">The Volume Shadow Copy Service (VSS) API provides both COM and C++ interfaces to support the creation of requesters and writers.</span></span>

## <a name="vss-requester-specific-interfaces"></a><span data-ttu-id="6fbc8-105">VSS Requester-Specific 介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-105">VSS Requester-Specific Interfaces</span></span>

-   [<span data-ttu-id="6fbc8-106">**>ivssbackupcomponents**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-106">**IVssBackupComponents**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [<span data-ttu-id="6fbc8-107">**IVssBackupComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-107">**IVssBackupComponentsEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [<span data-ttu-id="6fbc8-108">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-108">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [<span data-ttu-id="6fbc8-109">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-109">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [<span data-ttu-id="6fbc8-110">**IVssExamineWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-110">**IVssExamineWriterMetadata**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [<span data-ttu-id="6fbc8-111">**IVssExamineWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-111">**IVssExamineWriterMetadataEx**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [<span data-ttu-id="6fbc8-112">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-112">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [<span data-ttu-id="6fbc8-113">**IVssWMComponent**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-113">**IVssWMComponent**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [<span data-ttu-id="6fbc8-114">**IVssWriterComponentsExt**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-114">**IVssWriterComponentsExt**</span></span>](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a><span data-ttu-id="6fbc8-115">VSS Writer-Specific 介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-115">VSS Writer-Specific Interfaces</span></span>

-   [<span data-ttu-id="6fbc8-116">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-116">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [<span data-ttu-id="6fbc8-117">**IVssCreateWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-117">**IVssCreateWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [<span data-ttu-id="6fbc8-118">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-118">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [<span data-ttu-id="6fbc8-119">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-119">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [<span data-ttu-id="6fbc8-120">**IVssWriterComponents**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-120">**IVssWriterComponents**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a><span data-ttu-id="6fbc8-121">VSS 硬體 Provider-Specific 介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-121">VSS Hardware Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="6fbc8-122">**IVssAdmin**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-122">**IVssAdmin**</span></span>](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [<span data-ttu-id="6fbc8-123">**IVssHardwareSnapshotProvider**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-123">**IVssHardwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [<span data-ttu-id="6fbc8-124">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-124">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [<span data-ttu-id="6fbc8-125">**IVssProviderCreateSnapshotSet**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-125">**IVssProviderCreateSnapshotSet**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [<span data-ttu-id="6fbc8-126">**IVssProviderNotifications**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-126">**IVssProviderNotifications**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a><span data-ttu-id="6fbc8-127">VSS 軟體 Provider-Specific 介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-127">VSS Software Provider-Specific Interfaces</span></span>

-   [<span data-ttu-id="6fbc8-128">**IVssSoftwareSnapshotProvider**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-128">**IVssSoftwareSnapshotProvider**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a><span data-ttu-id="6fbc8-129">VSS 共用介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-129">VSS Shared Interfaces</span></span>

-   [<span data-ttu-id="6fbc8-130">**IVssAsync**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-130">**IVssAsync**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [<span data-ttu-id="6fbc8-131">**>ivsscomponent**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-131">**IVssComponent**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [<span data-ttu-id="6fbc8-132">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-132">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [<span data-ttu-id="6fbc8-133">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-133">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [<span data-ttu-id="6fbc8-134">**IVssEnumObject**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-134">**IVssEnumObject**</span></span>](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [<span data-ttu-id="6fbc8-135">**IVssWMDependency**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-135">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [<span data-ttu-id="6fbc8-136">**IVssWMFiledesc**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-136">**IVssWMFiledesc**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a><span data-ttu-id="6fbc8-137">VSS 管理介面</span><span class="sxs-lookup"><span data-stu-id="6fbc8-137">VSS Management Interfaces</span></span>

-   [<span data-ttu-id="6fbc8-138">**IVssDifferentialSoftwareSnapshotMgmt**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-138">**IVssDifferentialSoftwareSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [<span data-ttu-id="6fbc8-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-139">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [<span data-ttu-id="6fbc8-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-140">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [<span data-ttu-id="6fbc8-141">**IVssEnumMgmtObject**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-141">**IVssEnumMgmtObject**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [<span data-ttu-id="6fbc8-142">**IVssSnapshotMgmt**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-142">**IVssSnapshotMgmt**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [<span data-ttu-id="6fbc8-143">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="6fbc8-143">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
