---
title: '驗證層級常數 (Rpcdce) '
description: 這些值會指定驗證層級，指出提供來協助保護資料完整性的驗證數量。 每個層級都包含先前層級所提供的保護。
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509428"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="ccb2e-104">驗證層級常數</span><span class="sxs-lookup"><span data-stu-id="ccb2e-104">Authentication Level Constants</span></span>

<span data-ttu-id="ccb2e-105">這些值會指定驗證層級，指出提供來協助保護資料完整性的驗證數量。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="ccb2e-106">每個層級都包含先前層級所提供的保護。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="ccb2e-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="ccb2e-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="ccb2e-108">Description</span><span class="sxs-lookup"><span data-stu-id="ccb2e-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="ccb2e-109"><dt>**RPC \_C \_ 驗證 \_ 層級 \_ 預設值**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="ccb2e-110">告訴 DCOM 使用其一般安全性整體協商演算法來選擇驗證等級。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="ccb2e-111">如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="ccb2e-112"><dt>**RPC \_C \_ 驗證 \_ 層級 \_ 無**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="ccb2e-113">不執行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="ccb2e-114"><dt>**RPC \_C \_ 驗證 \_ LEVEL \_ CONNECT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="ccb2e-115">只有當用戶端建立與伺服器之間的關聯性時，才會驗證用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="ccb2e-116">資料包傳輸一律改用 RPC \_ 驗證 \_ 層級 \_ PKT。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="ccb2e-117"><dt>**RPC \_C \_ 驗證 \_ 層級 \_ 呼叫**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="ccb2e-118">當伺服器收到要求時，只會在每個遠端程序呼叫的開頭進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="ccb2e-119">資料包傳輸會改為使用 RPC \_ C \_ 驗證 \_ 層級 \_ PKT。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="ccb2e-120"><dt>**RPC \_C \_ 驗證 \_ LEVEL \_ PKT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="ccb2e-121">驗證收到的所有資料都是來自預期的用戶端。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="ccb2e-122"><dt>**RPC \_C \_ 驗證 \_ LEVEL \_ PKT \_ 完整性**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="ccb2e-123">驗證並確認在用戶端與伺服器之間傳送的資料都沒有修改。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="ccb2e-124"><dt>**RPC \_C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="ccb2e-125">驗證所有先前的層級，並加密每個遠端程序呼叫的引數值。</span><span class="sxs-lookup"><span data-stu-id="ccb2e-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="ccb2e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccb2e-126">Requirements</span></span>



| <span data-ttu-id="ccb2e-127">需求</span><span class="sxs-lookup"><span data-stu-id="ccb2e-127">Requirement</span></span> | <span data-ttu-id="ccb2e-128">值</span><span class="sxs-lookup"><span data-stu-id="ccb2e-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb2e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccb2e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb2e-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccb2e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ccb2e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccb2e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb2e-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccb2e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ccb2e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="ccb2e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccb2e-134"><dt>Rpcdce。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





