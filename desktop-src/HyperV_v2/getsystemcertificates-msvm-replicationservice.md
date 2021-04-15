---
description: 抓取主機系統上的系統憑證。
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Msvm_ReplicationService 類別的 GetSystemCertificates 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511009"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="033e1-103">Msvm ReplicationService 類別的 GetSystemCertificates 方法 \_</span><span class="sxs-lookup"><span data-stu-id="033e1-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="033e1-104">抓取主機系統上的系統憑證。</span><span class="sxs-lookup"><span data-stu-id="033e1-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="033e1-105">語法</span><span class="sxs-lookup"><span data-stu-id="033e1-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="033e1-106">參數</span><span class="sxs-lookup"><span data-stu-id="033e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="033e1-107">*EncodedCertificates* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="033e1-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="033e1-108">如果成功，則會接收本機電腦的個人存放區中可用的憑證。</span><span class="sxs-lookup"><span data-stu-id="033e1-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="033e1-109">每個專案都是基底64編碼的憑證字串。</span><span class="sxs-lookup"><span data-stu-id="033e1-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="033e1-110">您可以藉由建立 X509Certificate2 物件，將這個字串轉換成位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="033e1-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="033e1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="033e1-111">Return value</span></span>

<span data-ttu-id="033e1-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="033e1-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="033e1-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="033e1-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="033e1-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="033e1-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="033e1-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="033e1-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="033e1-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="033e1-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="033e1-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="033e1-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="033e1-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="033e1-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="033e1-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="033e1-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="033e1-126">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="033e1-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="033e1-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="033e1-127">Requirements</span></span>



| <span data-ttu-id="033e1-128">需求</span><span class="sxs-lookup"><span data-stu-id="033e1-128">Requirement</span></span> | <span data-ttu-id="033e1-129">值</span><span class="sxs-lookup"><span data-stu-id="033e1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="033e1-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="033e1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="033e1-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="033e1-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="033e1-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="033e1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="033e1-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="033e1-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="033e1-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="033e1-134">Namespace</span></span><br/>                | <span data-ttu-id="033e1-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="033e1-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="033e1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="033e1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="033e1-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="033e1-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="033e1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="033e1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="033e1-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="033e1-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="033e1-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="033e1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033e1-141">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="033e1-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




