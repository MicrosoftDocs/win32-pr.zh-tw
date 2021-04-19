---
title: Win32_TSApplicationFileExtensions 類別的 FileAssociations 方法
description: 掃描登錄以取得應用程式目前的檔案關聯。
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- FileAssociations 方法遠端桌面服務
- FileAssociations 方法遠端桌面服務，Win32_TSApplicationFileExtensions 類別
- Win32_TSApplicationFileExtensions 類別遠端桌面服務，FileAssociations 方法
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965942"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="55308-106">Win32 TSApplicationFileExtensions 類別的 FileAssociations 方法 \_</span><span class="sxs-lookup"><span data-stu-id="55308-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="55308-107">掃描登錄以取得應用程式目前的檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="55308-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="55308-108">語法</span><span class="sxs-lookup"><span data-stu-id="55308-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="55308-109">參數</span><span class="sxs-lookup"><span data-stu-id="55308-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55308-110">*AppPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55308-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55308-111">指定應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="55308-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="55308-112">*FileAssociations* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55308-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55308-113">成功完成時，會包含此應用程式的檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="55308-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55308-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="55308-114">Requirements</span></span>



| <span data-ttu-id="55308-115">需求</span><span class="sxs-lookup"><span data-stu-id="55308-115">Requirement</span></span> | <span data-ttu-id="55308-116">值</span><span class="sxs-lookup"><span data-stu-id="55308-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55308-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55308-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55308-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="55308-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="55308-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55308-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55308-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55308-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="55308-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="55308-121">Namespace</span></span><br/>                | <span data-ttu-id="55308-122">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="55308-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="55308-123">MOF</span><span class="sxs-lookup"><span data-stu-id="55308-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55308-124"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="55308-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="55308-125">DLL</span><span class="sxs-lookup"><span data-stu-id="55308-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55308-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55308-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55308-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55308-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55308-128">**Win32 \_ TSApplicationFileExtensions**</span><span class="sxs-lookup"><span data-stu-id="55308-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="55308-129">**Win32 \_ RDFileAssociation**</span><span class="sxs-lookup"><span data-stu-id="55308-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





