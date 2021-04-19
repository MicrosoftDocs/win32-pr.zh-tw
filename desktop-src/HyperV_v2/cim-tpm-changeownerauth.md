---
description: 變更 TPM 裝置的擁有者授權認證。 需要舊的和新的擁有者授權密碼。
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: CIM_TPM 類別的 ChangeOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974629"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="a6bb0-104">CIM TPM 類別的 ChangeOwnerAuth 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a6bb0-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="a6bb0-105">變更 TPM 裝置的擁有者授權認證。</span><span class="sxs-lookup"><span data-stu-id="a6bb0-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="a6bb0-106">需要舊的和新的擁有者授權密碼。</span><span class="sxs-lookup"><span data-stu-id="a6bb0-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bb0-107">語法</span><span class="sxs-lookup"><span data-stu-id="a6bb0-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="a6bb0-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6bb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bb0-109">*OldOwnerAuth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6bb0-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bb0-110">代表取得 TPM 裝置擁有權所需的舊擁有者授權認證。Cim **\_ SharedCredential** 的非 null 值可能需要 **cim \_ SharedCredential** 子類別。參數的 Secret 屬性。</span><span class="sxs-lookup"><span data-stu-id="a6bb0-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a6bb0-111">*NewOwnerAuth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6bb0-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bb0-112">代表取得 TPM 裝置擁有權所需的新擁有者授權認證。Cim **\_ SharedCredential** 的非 null 值可能需要 **cim \_ SharedCredential** 子類別。參數的 Secret 屬性。</span><span class="sxs-lookup"><span data-stu-id="a6bb0-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bb0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6bb0-113">Return value</span></span>

<span data-ttu-id="a6bb0-114">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a6bb0-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a6bb0-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a6bb0-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6bb0-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a6bb0-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a6bb0-117">**未知/未指定的錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="a6bb0-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a6bb0-118">**DMTF 保留** (3. 4095) </span><span class="sxs-lookup"><span data-stu-id="a6bb0-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="a6bb0-119">**方法保留** (4096. 32767) </span><span class="sxs-lookup"><span data-stu-id="a6bb0-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a6bb0-120">**指定的廠商** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a6bb0-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a6bb0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6bb0-121">Requirements</span></span>



| <span data-ttu-id="a6bb0-122">需求</span><span class="sxs-lookup"><span data-stu-id="a6bb0-122">Requirement</span></span> | <span data-ttu-id="a6bb0-123">值</span><span class="sxs-lookup"><span data-stu-id="a6bb0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bb0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6bb0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a6bb0-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6bb0-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a6bb0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6bb0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a6bb0-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a6bb0-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a6bb0-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a6bb0-128">Namespace</span></span><br/>                | <span data-ttu-id="a6bb0-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a6bb0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a6bb0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a6bb0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6bb0-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a6bb0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6bb0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a6bb0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6bb0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6bb0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6bb0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6bb0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bb0-135">**CIM \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="a6bb0-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




