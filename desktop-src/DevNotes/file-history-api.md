---
description: 檔案歷程記錄 API
ms.assetid: 7488BA36-DEBE-42F1-8A12-A2DB1DE8B827
title: 檔案歷程記錄 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb612a0bbbbd28b703a82bc65c5cd4d33640f760
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936194"
---
# <a name="file-history-api"></a><span data-ttu-id="d9cdf-103">檔案歷程記錄 API</span><span class="sxs-lookup"><span data-stu-id="d9cdf-103">File History API</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d9cdf-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="d9cdf-104">In this section</span></span>

-   [<span data-ttu-id="d9cdf-105">**FH \_ 備份 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-105">**FH\_BACKUP\_STATUS**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_backup_status)
-   [<span data-ttu-id="d9cdf-106">**FH \_ 裝置 \_ 驗證 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-106">**FH\_DEVICE\_VALIDATION\_RESULT**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_device_validation_result)
-   [<span data-ttu-id="d9cdf-107">**FH \_ 本機 \_ 原則 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-107">**FH\_LOCAL\_POLICY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_local_policy_type)
-   [<span data-ttu-id="d9cdf-108">**FH \_ 受保護 \_ 專案 \_ 類別目錄**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-108">**FH\_PROTECTED\_ITEM\_CATEGORY**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_protected_item_category)
-   [<span data-ttu-id="d9cdf-109">**FH \_ 保留 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-109">**FH\_RETENTION\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_retention_types)
-   [<span data-ttu-id="d9cdf-110">**FH \_ 目標 \_ 磁片磁碟機 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-110">**FH\_TARGET\_DRIVE\_TYPES**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_drive_types)
-   [<span data-ttu-id="d9cdf-111">**FH \_ 目標 \_ 屬性 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-111">**FH\_TARGET\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/Fhcfg/ne-fhcfg-fh_target_property_type)
-   [<span data-ttu-id="d9cdf-112">**FhConfigMgr**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-112">**FhConfigMgr**</span></span>](fhconfigmgr.md)
-   [<span data-ttu-id="d9cdf-113">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="d9cdf-113">FhManagew.exe</span></span>](fhmanagew-exe.md)
-   [<span data-ttu-id="d9cdf-114">**FhReassociation**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-114">**FhReassociation**</span></span>](fhreassociation.md)
-   [<span data-ttu-id="d9cdf-115">**FhServiceClosePipe**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-115">**FhServiceClosePipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceclosepipe)
-   [<span data-ttu-id="d9cdf-116">**FhServiceOpenPipe**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-116">**FhServiceOpenPipe**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceopenpipe)
-   [<span data-ttu-id="d9cdf-117">**FhServiceReloadConfiguration**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-117">**FhServiceReloadConfiguration**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicereloadconfiguration)
-   [<span data-ttu-id="d9cdf-118">**FhServiceBlockBackup**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-118">**FhServiceBlockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceblockbackup)
-   [<span data-ttu-id="d9cdf-119">**FhServiceStartBackup**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-119">**FhServiceStartBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestartbackup)
-   [<span data-ttu-id="d9cdf-120">**FhServiceStopBackup**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-120">**FhServiceStopBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhservicestopbackup)
-   [<span data-ttu-id="d9cdf-121">**FhServiceUnblockBackup**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-121">**FhServiceUnblockBackup**</span></span>](/windows/desktop/api/FhSvcCtl/nf-fhsvcctl-fhserviceunblockbackup)
-   [<span data-ttu-id="d9cdf-122">**IFhConfigMgr**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-122">**IFhConfigMgr**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr)
-   [<span data-ttu-id="d9cdf-123">**IFhReassociation**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-123">**IFhReassociation**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation)
-   [<span data-ttu-id="d9cdf-124">**IFhScopeIterator**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-124">**IFhScopeIterator**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhscopeiterator)
-   [<span data-ttu-id="d9cdf-125">**IFhTarget**</span><span class="sxs-lookup"><span data-stu-id="d9cdf-125">**IFhTarget**</span></span>](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhtarget)

 

 



