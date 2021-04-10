---
title: Revoke Win32_TSIssuedLicense 類別的方法
description: 撤銷遠端桌面服務的每一裝置用戶端存取授權 (RDS \ 160;Win32 TSIssuedLicense 物件所代表的每一裝置 Cal) \_ 。 這不是靜態函數。
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Revoke 方法遠端桌面服務
- Revoke 方法遠端桌面服務，Win32_TSIssuedLicense 類別
- Win32_TSIssuedLicense 類別遠端桌面服務、Revoke 方法
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686488"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="b648f-107">Revoke Win32 \_ TSIssuedLicense 類別的方法</span><span class="sxs-lookup"><span data-stu-id="b648f-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="b648f-108">撤銷遠端桌面服務的每一裝置用戶端存取授權 (由 [**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md) 物件所代表的 RDS 每一裝置 cal) 。</span><span class="sxs-lookup"><span data-stu-id="b648f-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="b648f-109">這不是靜態函數。</span><span class="sxs-lookup"><span data-stu-id="b648f-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b648f-110">語法</span><span class="sxs-lookup"><span data-stu-id="b648f-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="b648f-111">參數</span><span class="sxs-lookup"><span data-stu-id="b648f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b648f-112">*RevokableCals* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b648f-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b648f-113">與可撤銷的目前物件相同類型的 RDS Cal 數目。</span><span class="sxs-lookup"><span data-stu-id="b648f-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="b648f-114">*NextRevokeAllowedOn* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b648f-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b648f-115">系統管理員可以在下一次嘗試撤銷授權的日期。</span><span class="sxs-lookup"><span data-stu-id="b648f-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="b648f-116">當 **revoke** 方法呼叫失敗，因為已達到最大撤銷計數，此參數只會包含有效的資料。</span><span class="sxs-lookup"><span data-stu-id="b648f-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b648f-117">備註</span><span class="sxs-lookup"><span data-stu-id="b648f-117">Remarks</span></span>

<span data-ttu-id="b648f-118">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b648f-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b648f-119">只有 RDS 每一裝置的 Cal 可以撤銷。</span><span class="sxs-lookup"><span data-stu-id="b648f-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="b648f-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b648f-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b648f-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b648f-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b648f-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b648f-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b648f-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b648f-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b648f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b648f-124">Requirements</span></span>



| <span data-ttu-id="b648f-125">需求</span><span class="sxs-lookup"><span data-stu-id="b648f-125">Requirement</span></span> | <span data-ttu-id="b648f-126">值</span><span class="sxs-lookup"><span data-stu-id="b648f-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b648f-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b648f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b648f-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="b648f-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b648f-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b648f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b648f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b648f-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b648f-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="b648f-131">Namespace</span></span><br/>                | <span data-ttu-id="b648f-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b648f-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b648f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b648f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b648f-134"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b648f-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b648f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b648f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b648f-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b648f-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b648f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b648f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b648f-138">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="b648f-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

