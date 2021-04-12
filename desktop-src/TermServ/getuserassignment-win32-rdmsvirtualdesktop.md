---
title: Win32_RDMSVirtualDesktop 類別的 GetUserAssignment 方法
description: 抓取指派給虛擬桌面使用者的使用者名稱和功能變數名稱。
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- GetUserAssignment 方法遠端桌面服務
- GetUserAssignment 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetUserAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384901"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="4d04b-106">Win32 RDMSVirtualDesktop 類別的 GetUserAssignment 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4d04b-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="4d04b-107">抓取指派給虛擬桌面使用者的使用者名稱和功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="4d04b-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d04b-108">語法</span><span class="sxs-lookup"><span data-stu-id="4d04b-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="4d04b-109">參數</span><span class="sxs-lookup"><span data-stu-id="4d04b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d04b-110">使用者 *名稱* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d04b-111">接收使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="4d04b-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="4d04b-112">*UserDomain* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d04b-113">接收功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="4d04b-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d04b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d04b-114">Return value</span></span>

<span data-ttu-id="4d04b-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4d04b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d04b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d04b-116">Requirements</span></span>



| <span data-ttu-id="4d04b-117">需求</span><span class="sxs-lookup"><span data-stu-id="4d04b-117">Requirement</span></span> | <span data-ttu-id="4d04b-118">值</span><span class="sxs-lookup"><span data-stu-id="4d04b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d04b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d04b-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="4d04b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4d04b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d04b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d04b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d04b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4d04b-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d04b-123">Namespace</span></span><br/>                | <span data-ttu-id="4d04b-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="4d04b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4d04b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4d04b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d04b-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d04b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d04b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d04b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d04b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d04b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4d04b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d04b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d04b-130">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="4d04b-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





