---
title: TB 函數
description: TBS 提供下列功能。
ms.assetid: df2d3e36-0a27-4cc0-bcb2-709eb6bedeac
keywords:
- TPM 基礎服務 TB、函數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1b34f2dfbe18ef2230838ff4ba9ec2241d3cc2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376048"
---
# <a name="tbs-functions"></a><span data-ttu-id="a9adb-104">TB 函數</span><span class="sxs-lookup"><span data-stu-id="a9adb-104">TBS Functions</span></span>

<span data-ttu-id="a9adb-105">TBS 提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="a9adb-105">TBS provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9adb-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="a9adb-106">In this section</span></span>



| <span data-ttu-id="a9adb-107">主題</span><span class="sxs-lookup"><span data-stu-id="a9adb-107">Topic</span></span>                                                                                       | <span data-ttu-id="a9adb-108">描述</span><span class="sxs-lookup"><span data-stu-id="a9adb-108">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9adb-109">**Tbsi \_ 內容 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="a9adb-109">**Tbsi\_Context\_Create**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_context_create)<br/>                            | <span data-ttu-id="a9adb-110">建立可以用來將命令傳遞至 TBS 的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a9adb-110">Creates a context handle that can be used to pass commands to TBS.</span></span><br/>                                                                               |
| <span data-ttu-id="a9adb-111">[**Tbsi \_ \_ \_ 從記錄檔建立證明 \_**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9adb-111">[**Tbsi\_Create\_Attestation\_From\_Log**](/previous-versions/windows/desktop/legacy/dn455155(v=vs.85))</span></span><br/> | <span data-ttu-id="a9adb-112">從 TCG 記錄檔中解壓縮 TrustPoint 來建立證明。</span><span class="sxs-lookup"><span data-stu-id="a9adb-112">Creates an attestation by extracting a TrustPoint from a TCG log.</span></span><br/>                                                                                |
| [<span data-ttu-id="a9adb-113">**Tbsi \_ GetDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="a9adb-113">**Tbsi\_GetDeviceInfo**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_getdeviceinfo)<br/>                                | <span data-ttu-id="a9adb-114">取得電腦上的 TPM 版本。</span><span class="sxs-lookup"><span data-stu-id="a9adb-114">Obtains the version of the TPM on the computer.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="a9adb-115">**Tbsi \_ Get \_ OwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="a9adb-115">**Tbsi\_Get\_OwnerAuth**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_ownerauth)<br/>                               | <span data-ttu-id="a9adb-116">如果本機登錄中有可用的資訊，則抓取 TPM 的擁有者授權。</span><span class="sxs-lookup"><span data-stu-id="a9adb-116">Retrieves the owner authorization of the TPM if the information is available in the local registry.</span></span> <br/>                                             |
| [<span data-ttu-id="a9adb-117">**Tbsi \_ 取得 \_ TCG \_ 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="a9adb-117">**Tbsi\_Get\_TCG\_Log**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log)<br/>                                  | <span data-ttu-id="a9adb-118">抓取最新的 Windows 開機設定記錄 (WBCL) ，也稱為 TCG 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a9adb-118">Retrieves the most recent Windows Boot Configuration Log (WBCL), also referred to as a TCG log.</span></span><br/>                                                  |
| [<span data-ttu-id="a9adb-119">**Tbsi \_ 取得 \_ TCG \_ 記錄檔 \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="a9adb-119">**Tbsi\_Get\_TCG\_Log\_Ex**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_get_tcg_log_ex)<br/>                           | <span data-ttu-id="a9adb-120">取得指定類型的 Windows 開機設定記錄 (WBCL) ，也稱為 TCG 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a9adb-120">Gets the Windows Boot Configuration Log (WBCL), also referred to as the TCG log, of the specified type.</span></span><br/>                                          |
| <span data-ttu-id="a9adb-121">[**Tbsi \_ 取得 \_ TCG \_ 記錄**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9adb-121">[**Tbsi\_Get\_TCG\_Logs**](/previous-versions/windows/desktop/legacy/dn455156(v=vs.85))</span></span><br/>                                | <span data-ttu-id="a9adb-122">取得一或多個 Windows 開機設定記錄 (WBCL) ，也稱為 TCG 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a9adb-122">Get one or more Windows Boot Configuration Logs (WBCL), also referred to as the TCG logs.</span></span><br/>                                                        |
| [<span data-ttu-id="a9adb-123">**Tbsi \_ 實體 \_ 存在性 \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="a9adb-123">**Tbsi\_Physical\_Presence\_Command**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_physical_presence_command)<br/>     | <span data-ttu-id="a9adb-124">透過 TB 傳遞實體存在性 ACPI 命令至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="a9adb-124">Passes a physical presence ACPI command through TBS to the driver.</span></span><br/>                                                                               |
| [<span data-ttu-id="a9adb-125">**Tbsi \_ Revoke \_ 證明**</span><span class="sxs-lookup"><span data-stu-id="a9adb-125">**Tbsi\_Revoke\_Attestation**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsi_revoke_attestation)<br/>                     | <span data-ttu-id="a9adb-126">如果 ELAM 驅動程式偵測到原則違規 (rootkit，例如) ，則會使 PCRs 失效。</span><span class="sxs-lookup"><span data-stu-id="a9adb-126">Invalidates the PCRs if the ELAM driver detects a policy-violation (a rootkit, for example).</span></span><br/>                                                     |
| [<span data-ttu-id="a9adb-127">**Tbsip \_ Cancel \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="a9adb-127">**Tbsip\_Cancel\_Commands**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsip_cancel_commands)<br/>                        | <span data-ttu-id="a9adb-128">取消指定內容的所有未完成命令。</span><span class="sxs-lookup"><span data-stu-id="a9adb-128">Cancels all outstanding commands for the specified context.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a9adb-129">**Tbsip \_ 內容 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="a9adb-129">**Tbsip\_Context\_Close**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsip_context_close)<br/>                            | <span data-ttu-id="a9adb-130">關閉內容控制碼，此控制碼會釋放與內容（以 TB 為）相關聯的資源，並關閉用來與 TBS 通訊的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a9adb-130">Closes a context handle, which releases resources associated with the context in TBS and closes the binding handle used to communicate with TBS.</span></span><br/> |
| [<span data-ttu-id="a9adb-131">**Tbsip \_ Submit \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="a9adb-131">**Tbsip\_Submit\_Command**</span></span>](/windows/desktop/api/Tbs/nf-tbs-tbsip_submit_command)<br/>                          | <span data-ttu-id="a9adb-132">將可信賴平臺模組 (TPM) 命令提交至 TPM 基底服務， (TB) 進行處理。</span><span class="sxs-lookup"><span data-stu-id="a9adb-132">Submits a Trusted Platform Module (TPM) command to TPM Base Services (TBS) for processing.</span></span><br/>                                                       |



 

 

