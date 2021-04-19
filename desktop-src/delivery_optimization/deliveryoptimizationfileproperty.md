---
title: 'DeliveryOptimizationFileProperty 列舉 (>deliveryoptimization) '
description: DeliveryOptimizationFileProperty 列舉會指定 DO 檔案的選擇性屬性識別碼。
keywords:
- DeliveryOptimizationFileProperty 列舉
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969777"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="ae8d4-104">DeliveryOptimizationFileProperty 列舉</span><span class="sxs-lookup"><span data-stu-id="ae8d4-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="ae8d4-105">DeliveryOptimizationFileProperty 列舉會指定 DO 檔案的選擇性屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="ae8d4-106">此列舉會在 IDeliveryOptimizationFile2 介面中使用，其中類型為 VARIANT 的屬性值已傳遞</span><span class="sxs-lookup"><span data-stu-id="ae8d4-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae8d4-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="ae8d4-108">常數</span><span class="sxs-lookup"><span data-stu-id="ae8d4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ae8d4-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="ae8d4-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="ae8d4-110">DOFilePropertyId_DecryptionInfo 屬性識別碼會以 JSON 字串的形式來設定解密資訊。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="ae8d4-111">DOFilePropertyId_DecryptionInfo 是 VT_BSTR 類型的僅限寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ae8d4-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="ae8d4-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="ae8d4-113">DOFilePropertyId_IntegrityCheckInfo 屬性識別碼會將片段雜湊檔設定 (PHF) 位置，以供執行以針對下載的內容執行執行時間完整性檢查。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="ae8d4-114">DOFilePropertyId_IntegrityCheckInfo 是 VT_BSTR 類型的僅限寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ae8d4-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="ae8d4-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="ae8d4-116">DOFilePropertyId_IntegrityCheckMandatory 屬性識別碼會設定布林值旗標，指出 PHF 的使用是否為強制性。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="ae8d4-117">若為 TRUE，當完整性檢查失敗時，將會中止下載。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="ae8d4-118">DOFilePropertyId_IntegrityCheckMandatory 是 VT_BOOL 類型的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="ae8d4-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="ae8d4-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="ae8d4-120">DOFilePropertyId_DownloadSinkFilePath 屬性識別碼會設定要在其中儲存所下載元件的完整檔案系統位置。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="ae8d4-121">DOFilePropertyId_DownloadSinkFilePath 的類型 VT_BSTR。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ae8d4-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="ae8d4-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="ae8d4-123">DOFilePropertyId_DownloadSinkMemoryStream 屬性識別碼已被取代。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="ae8d4-124">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ae8d4-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ae8d4-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="ae8d4-126">DOFilePropertyId_TotalSizeBytes 屬性識別碼會指定下載大小總計。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="ae8d4-127">DOFilePropertyId_TotalSizeBytes 的類型 VT_UI8。</span><span class="sxs-lookup"><span data-stu-id="ae8d4-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae8d4-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae8d4-128">Requirements</span></span>

| <span data-ttu-id="ae8d4-129">需求</span><span class="sxs-lookup"><span data-stu-id="ae8d4-129">Requirement</span></span> | <span data-ttu-id="ae8d4-130">值</span><span class="sxs-lookup"><span data-stu-id="ae8d4-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ae8d4-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae8d4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ae8d4-132">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae8d4-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="ae8d4-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae8d4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ae8d4-134">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae8d4-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="ae8d4-135">標頭</span><span class="sxs-lookup"><span data-stu-id="ae8d4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae8d4-136"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae8d4-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
