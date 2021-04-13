---
title: Win32_RDMSVirtualDesktopCollection 類別的 SchedulePatch 方法
description: 排程軟體更新布建作業，此作業會在虛擬桌面集合中的虛擬機器上安裝軟體更新。
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- SchedulePatch 方法遠端桌面服務
- SchedulePatch 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，SchedulePatch 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465112"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="44508-106">Win32 RDMSVirtualDesktopCollection 類別的 SchedulePatch 方法 \_</span><span class="sxs-lookup"><span data-stu-id="44508-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="44508-107">排程軟體更新布建作業，此作業會在虛擬桌面集合中的虛擬機器上安裝軟體更新。</span><span class="sxs-lookup"><span data-stu-id="44508-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="44508-108">語法</span><span class="sxs-lookup"><span data-stu-id="44508-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="44508-109">參數</span><span class="sxs-lookup"><span data-stu-id="44508-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44508-110">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44508-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="44508-111">系統將不會登出虛擬機器的使用者，直到 *ForceLogOffTime* 參數中指定的時間為止。</span><span class="sxs-lookup"><span data-stu-id="44508-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="44508-112">安裝更新的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="44508-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="44508-113">*ForceLogOffTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44508-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44508-114">系統將登出虛擬機器使用者的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="44508-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="44508-115">*JobInputXml* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44508-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44508-116">XML 格式的字串，其中包含軟體更新作業資訊。</span><span class="sxs-lookup"><span data-stu-id="44508-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44508-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="44508-117">Return value</span></span>

<span data-ttu-id="44508-118">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="44508-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44508-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="44508-119">Requirements</span></span>



| <span data-ttu-id="44508-120">需求</span><span class="sxs-lookup"><span data-stu-id="44508-120">Requirement</span></span> | <span data-ttu-id="44508-121">值</span><span class="sxs-lookup"><span data-stu-id="44508-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="44508-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44508-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44508-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="44508-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="44508-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44508-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44508-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44508-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="44508-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="44508-126">Namespace</span></span><br/>                | <span data-ttu-id="44508-127">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="44508-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="44508-128">MOF</span><span class="sxs-lookup"><span data-stu-id="44508-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44508-129"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="44508-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="44508-130">DLL</span><span class="sxs-lookup"><span data-stu-id="44508-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44508-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44508-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="44508-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44508-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44508-133">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="44508-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





