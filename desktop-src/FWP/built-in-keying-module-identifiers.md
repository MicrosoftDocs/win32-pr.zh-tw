---
title: '內建的加密模組識別碼 (Fwpmu .h) '
description: 內建于 Windows 篩選平台 (WFP) 之金鑰模組的識別碼，會由 GUID 表示。
ms.assetid: ba3aaf0f-5524-4d61-bb74-e4714b11b2a9
topic_type:
- apiref
api_name:
- FWPM_KEYING_MODULE_IKE
- FWPM_KEYING_MODULE_IKEV2
- FWPM_KEYING_MODULE_AUTHIP
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9e6feb726a62de02130d64cef27cd9078395b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935045"
---
# <a name="built-in-keying-module-identifiers"></a><span data-ttu-id="b0a22-103">內建的加密模組識別碼</span><span class="sxs-lookup"><span data-stu-id="b0a22-103">Built-in Keying Module Identifiers</span></span>

<span data-ttu-id="b0a22-104">內建于 Windows 篩選平台 (WFP) 之金鑰模組的識別碼，會由 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="b0a22-104">The identifiers for the keying modules that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="b0a22-105">這些識別碼的定義如下。</span><span class="sxs-lookup"><span data-stu-id="b0a22-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="b0a22-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**FWPM \_ 加密 \_ 模組 \_ IKE**</span><span class="sxs-lookup"><span data-stu-id="b0a22-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**FWPM\_KEYING\_MODULE\_IKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b0a22-107">網際網路金鑰交換 (IKE) 的加密模組。</span><span class="sxs-lookup"><span data-stu-id="b0a22-107">Internet Key Exchange (IKE) keying module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a22-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**FWPM \_ 加密 \_ 模組 \_ IKEV2**</span><span class="sxs-lookup"><span data-stu-id="b0a22-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**FWPM\_KEYING\_MODULE\_IKEV2**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b0a22-109">網際網路金鑰交換第2版 (IKEv2) 鍵控模組。</span><span class="sxs-lookup"><span data-stu-id="b0a22-109">Internet Key Exchange version 2 (IKEv2) keying module.</span></span>

> [!Note]  
> <span data-ttu-id="b0a22-110">僅適用于 Windows Server 2008 R2 和 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="b0a22-110">Available only on Windows Server 2008 R2 and Windows 7.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="b0a22-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**FWPM \_ 加密 \_ 模組 \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="b0a22-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**FWPM\_KEYING\_MODULE\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b0a22-112">AuthIP 金鑰模組。</span><span class="sxs-lookup"><span data-stu-id="b0a22-112">AuthIP keying module.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0a22-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0a22-113">Requirements</span></span>



| <span data-ttu-id="b0a22-114">需求</span><span class="sxs-lookup"><span data-stu-id="b0a22-114">Requirement</span></span> | <span data-ttu-id="b0a22-115">值</span><span class="sxs-lookup"><span data-stu-id="b0a22-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a22-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0a22-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a22-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0a22-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b0a22-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0a22-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a22-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0a22-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b0a22-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b0a22-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0a22-121"><dt>Fwpmu。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0a22-121"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





