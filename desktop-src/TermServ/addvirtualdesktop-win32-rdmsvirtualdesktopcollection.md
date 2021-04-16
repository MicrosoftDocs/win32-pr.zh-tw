---
title: Win32_RDMSVirtualDesktopCollection 類別的 AddVirtualDesktop 方法
description: 將虛擬桌面新增至虛擬桌面集合。
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- AddVirtualDesktop 方法遠端桌面服務
- AddVirtualDesktop 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，AddVirtualDesktop 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508388"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="eda2f-106">Win32 RDMSVirtualDesktopCollection 類別的 AddVirtualDesktop 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eda2f-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="eda2f-107">將虛擬桌面新增至虛擬桌面集合。</span><span class="sxs-lookup"><span data-stu-id="eda2f-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda2f-108">語法</span><span class="sxs-lookup"><span data-stu-id="eda2f-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="eda2f-109">參數</span><span class="sxs-lookup"><span data-stu-id="eda2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eda2f-110">*VMName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eda2f-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eda2f-111">裝載虛擬桌面的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="eda2f-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eda2f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="eda2f-112">Return value</span></span>

<span data-ttu-id="eda2f-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eda2f-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eda2f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="eda2f-114">Requirements</span></span>



| <span data-ttu-id="eda2f-115">需求</span><span class="sxs-lookup"><span data-stu-id="eda2f-115">Requirement</span></span> | <span data-ttu-id="eda2f-116">值</span><span class="sxs-lookup"><span data-stu-id="eda2f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eda2f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eda2f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eda2f-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="eda2f-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="eda2f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eda2f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eda2f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eda2f-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="eda2f-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="eda2f-121">Namespace</span></span><br/>                | <span data-ttu-id="eda2f-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="eda2f-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="eda2f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="eda2f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eda2f-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="eda2f-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="eda2f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eda2f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eda2f-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eda2f-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="eda2f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eda2f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda2f-128">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="eda2f-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





