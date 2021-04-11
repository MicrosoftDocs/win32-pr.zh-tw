---
title: Win32_TSApplicationFileExtensions 類別的 FileExtensions 方法
description: 提供應用程式所處理的副檔名清單。
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- FileExtensions 方法遠端桌面服務
- FileExtensions 方法遠端桌面服務，Win32_TSApplicationFileExtensions 類別
- Win32_TSApplicationFileExtensions 類別遠端桌面服務，FileExtensions 方法
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934974"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="e7a47-106">Win32 TSApplicationFileExtensions 類別的 FileExtensions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e7a47-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="e7a47-107">提供應用程式所處理的副檔名清單。</span><span class="sxs-lookup"><span data-stu-id="e7a47-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a47-108">語法</span><span class="sxs-lookup"><span data-stu-id="e7a47-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="e7a47-109">參數</span><span class="sxs-lookup"><span data-stu-id="e7a47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7a47-110">*AppPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-111">應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="e7a47-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="e7a47-112">*擴充* \[ 功能擴展\]</span><span class="sxs-lookup"><span data-stu-id="e7a47-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a47-113">應用程式所處理的副檔名。</span><span class="sxs-lookup"><span data-stu-id="e7a47-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7a47-114">備註</span><span class="sxs-lookup"><span data-stu-id="e7a47-114">Remarks</span></span>

<span data-ttu-id="e7a47-115">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e7a47-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e7a47-116">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e7a47-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e7a47-117">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e7a47-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e7a47-118">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e7a47-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e7a47-119">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e7a47-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a47-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7a47-120">Requirements</span></span>



| <span data-ttu-id="e7a47-121">需求</span><span class="sxs-lookup"><span data-stu-id="e7a47-121">Requirement</span></span> | <span data-ttu-id="e7a47-122">值</span><span class="sxs-lookup"><span data-stu-id="e7a47-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a47-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7a47-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a47-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="e7a47-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e7a47-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7a47-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a47-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7a47-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7a47-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="e7a47-127">Namespace</span></span><br/>                | <span data-ttu-id="e7a47-128">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e7a47-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e7a47-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e7a47-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7a47-130"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7a47-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="e7a47-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a47-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7a47-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a47-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a47-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7a47-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a47-134">**Win32 \_ TSApplicationFileExtensions**</span><span class="sxs-lookup"><span data-stu-id="e7a47-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

