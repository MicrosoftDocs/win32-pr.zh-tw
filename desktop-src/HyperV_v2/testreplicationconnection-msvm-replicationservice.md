---
description: 確認是否可以從目前的主機系統啟用複寫到指定的復原系統。
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Msvm_ReplicationService 類別的 TestReplicationConnection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973812"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a4d34-103">Msvm ReplicationService 類別的 TestReplicationConnection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a4d34-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a4d34-104">確認是否可以從目前的主機系統啟用複寫到指定的復原系統。</span><span class="sxs-lookup"><span data-stu-id="a4d34-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d34-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4d34-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a4d34-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4d34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4d34-107">*RecoveryConnectionPoint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d34-108">連接點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d34-108">The name of the connection point.</span></span> <span data-ttu-id="a4d34-109">若為復原叢集，這就是 broker CAP 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d34-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="a4d34-110">若是獨立的復原伺服器，這就是主機系統名稱。</span><span class="sxs-lookup"><span data-stu-id="a4d34-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="a4d34-111">*RecoveryServerPortNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d34-112">復原連接點埠號碼。</span><span class="sxs-lookup"><span data-stu-id="a4d34-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="a4d34-113">*AuthenticationType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d34-114">復原驗證配置。</span><span class="sxs-lookup"><span data-stu-id="a4d34-114">The recovery authentication scheme.</span></span> <span data-ttu-id="a4d34-115">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="a4d34-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="a4d34-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**整合式驗證** (1) </span><span class="sxs-lookup"><span data-stu-id="a4d34-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a4d34-117">Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="a4d34-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="a4d34-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>以 **憑證為基礎的驗證** (2) </span><span class="sxs-lookup"><span data-stu-id="a4d34-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a4d34-119">以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="a4d34-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a4d34-120">*CertificateThumbPrint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d34-121">當 *AuthenticationType* 參數是以憑證為基礎的驗證時，所要使用的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a4d34-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="a4d34-122">*BypassProxyServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d34-123">連接到複本伺服器時，請略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a4d34-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="a4d34-124">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4d34-125">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="a4d34-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4d34-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4d34-126">Return value</span></span>

<span data-ttu-id="a4d34-127">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a4d34-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a4d34-128">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a4d34-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-129">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a4d34-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-130">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="a4d34-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-131">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="a4d34-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-132">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="a4d34-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-133">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="a4d34-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-134">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="a4d34-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-135">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="a4d34-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-136">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="a4d34-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-137">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="a4d34-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-138">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="a4d34-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-139">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="a4d34-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-140">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="a4d34-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a4d34-141">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="a4d34-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a4d34-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4d34-142">Requirements</span></span>



| <span data-ttu-id="a4d34-143">需求</span><span class="sxs-lookup"><span data-stu-id="a4d34-143">Requirement</span></span> | <span data-ttu-id="a4d34-144">值</span><span class="sxs-lookup"><span data-stu-id="a4d34-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d34-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4d34-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d34-146">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4d34-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4d34-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d34-148">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4d34-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4d34-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4d34-149">Namespace</span></span><br/>                | <span data-ttu-id="a4d34-150">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a4d34-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4d34-151">MOF</span><span class="sxs-lookup"><span data-stu-id="a4d34-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4d34-152"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a4d34-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4d34-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d34-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d34-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4d34-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4d34-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4d34-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4d34-156">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="a4d34-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

