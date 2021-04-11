---
title: Win32_TSSessionDirectory 類別的 CreateUserDiskTemplate 方法
description: 建立使用者磁片範本。
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- CreateUserDiskTemplate 方法遠端桌面服務
- CreateUserDiskTemplate 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，CreateUserDiskTemplate 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094047"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="eed60-106">Win32 TSSessionDirectory 類別的 CreateUserDiskTemplate 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eed60-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="eed60-107">建立使用者磁片範本。</span><span class="sxs-lookup"><span data-stu-id="eed60-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed60-108">語法</span><span class="sxs-lookup"><span data-stu-id="eed60-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="eed60-109">參數</span><span class="sxs-lookup"><span data-stu-id="eed60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed60-110">*UserDisksStorageUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eed60-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed60-111">儲存所有使用者磁片之共用的位置。</span><span class="sxs-lookup"><span data-stu-id="eed60-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="eed60-112">*UserDiskMaxSizeInGB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eed60-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eed60-113">所有使用者磁片的大小上限（以 gb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="eed60-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eed60-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="eed60-114">Requirements</span></span>



| <span data-ttu-id="eed60-115">需求</span><span class="sxs-lookup"><span data-stu-id="eed60-115">Requirement</span></span> | <span data-ttu-id="eed60-116">值</span><span class="sxs-lookup"><span data-stu-id="eed60-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eed60-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eed60-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eed60-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="eed60-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eed60-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eed60-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eed60-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eed60-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="eed60-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="eed60-121">Namespace</span></span><br/>                | <span data-ttu-id="eed60-122">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="eed60-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="eed60-123">MOF</span><span class="sxs-lookup"><span data-stu-id="eed60-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eed60-124"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="eed60-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eed60-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eed60-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eed60-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eed60-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed60-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eed60-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed60-128">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="eed60-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





