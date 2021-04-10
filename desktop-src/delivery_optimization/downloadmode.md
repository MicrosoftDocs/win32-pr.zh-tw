---
title: 'DownloadMode 列舉 (>deliveryoptimization) '
description: 定義傳遞最佳化使用的不同下載模式。
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- 略過「傳遞最佳化」並改用 BITS。 例如，選取此模式即可讓用戶端使用 BranchCache。 列舉型別
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025014"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="514a0-106">DownloadMode 列舉</span><span class="sxs-lookup"><span data-stu-id="514a0-106">DownloadMode enumeration</span></span>

<span data-ttu-id="514a0-107">定義傳遞最佳化使用的不同下載模式。</span><span class="sxs-lookup"><span data-stu-id="514a0-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="514a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="514a0-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="514a0-109">常數</span><span class="sxs-lookup"><span data-stu-id="514a0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="514a0-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="514a0-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="514a0-111">此設定會停用對等快取，但仍可讓傳遞最佳化從 Microsoft 伺服器下載內容。</span><span class="sxs-lookup"><span data-stu-id="514a0-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="514a0-112">此模式會使用「傳遞最佳化」雲端服務所提供的其他中繼資料，達到無對等、可靠且有效率的下載體驗。</span><span class="sxs-lookup"><span data-stu-id="514a0-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="514a0-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="514a0-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="514a0-114">這個預設的「傳遞最佳化」操作模式可啟用相同網路上的對等共用。</span><span class="sxs-lookup"><span data-stu-id="514a0-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="514a0-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="514a0-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="514a0-116">當設定群組模式時，系統會根據裝置的 Active Directory Domain Services (AD DS) 網站 (Windows 10、1607版) 或裝置驗證的網域，以 (Windows 10 1511 版) 來自動選取群組。</span><span class="sxs-lookup"><span data-stu-id="514a0-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="514a0-117">在群組模式中，會跨內部子網路、在屬於相同群組的裝置 (包括遠端辦公室中的裝置) 之間進行對等互連。</span><span class="sxs-lookup"><span data-stu-id="514a0-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="514a0-118">您可以使用 GroupID 選項來建立自己的自訂群組，而不受網域和 AD DS 網站影響。</span><span class="sxs-lookup"><span data-stu-id="514a0-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="514a0-119">對於大部分組織而言，若要透過「傳遞最佳化」實現頻寬最佳化，建議使用群組下載模式的選項。</span><span class="sxs-lookup"><span data-stu-id="514a0-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="514a0-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="514a0-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="514a0-121">針對「傳遞最佳化」啟用網際網路對等來源。</span><span class="sxs-lookup"><span data-stu-id="514a0-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="514a0-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="514a0-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="514a0-123">簡單模式會完全停用「傳遞最佳化」雲端服務 (針對離線環境)。</span><span class="sxs-lookup"><span data-stu-id="514a0-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="514a0-124">當「傳遞最佳化」雲端服務無法使用、無法連線或當內容檔案大小小於 10 MB 時，「傳遞最佳化」會自動切換成這種模式。</span><span class="sxs-lookup"><span data-stu-id="514a0-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="514a0-125">在此模式下，「傳遞最佳化」會在沒有對等快取下提供可靠的下載體驗。</span><span class="sxs-lookup"><span data-stu-id="514a0-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="514a0-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="514a0-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="514a0-127">略過「傳遞最佳化」並改用 BITS。</span><span class="sxs-lookup"><span data-stu-id="514a0-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="514a0-128">例如，選取此模式即可讓用戶端使用 BranchCache。</span><span class="sxs-lookup"><span data-stu-id="514a0-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="514a0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="514a0-129">Requirements</span></span>

| <span data-ttu-id="514a0-130">需求</span><span class="sxs-lookup"><span data-stu-id="514a0-130">Requirement</span></span> | <span data-ttu-id="514a0-131">值</span><span class="sxs-lookup"><span data-stu-id="514a0-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="514a0-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="514a0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="514a0-133">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="514a0-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="514a0-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="514a0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="514a0-135">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="514a0-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="514a0-136">標頭</span><span class="sxs-lookup"><span data-stu-id="514a0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="514a0-137"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="514a0-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
