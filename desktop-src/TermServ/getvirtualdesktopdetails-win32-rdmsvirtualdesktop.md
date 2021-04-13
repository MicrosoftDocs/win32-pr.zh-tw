---
title: Win32_RDMSVirtualDesktop 類別的 GetVirtualDesktopDetails 方法
description: 抓取虛擬桌面的其他相關資訊。
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopDetails 方法遠端桌面服務
- GetVirtualDesktopDetails 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetVirtualDesktopDetails 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465793"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="6810c-106">Win32 RDMSVirtualDesktop 類別的 GetVirtualDesktopDetails 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6810c-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="6810c-107">抓取虛擬桌面的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6810c-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="6810c-108">語法</span><span class="sxs-lookup"><span data-stu-id="6810c-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="6810c-109">參數</span><span class="sxs-lookup"><span data-stu-id="6810c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6810c-110">*RAMSizeInMB* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6810c-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6810c-111">接收指派給虛擬桌面的 RAM 數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6810c-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6810c-112">*RemoteFXEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6810c-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6810c-113">接收值，指出虛擬桌面上是否已啟用 RemoteFX。</span><span class="sxs-lookup"><span data-stu-id="6810c-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="6810c-114">如果已啟用 RemoteFX，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6810c-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6810c-115">*OSVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6810c-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6810c-116">接收虛擬桌面的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="6810c-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6810c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6810c-117">Return value</span></span>

<span data-ttu-id="6810c-118">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6810c-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6810c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6810c-119">Requirements</span></span>



| <span data-ttu-id="6810c-120">需求</span><span class="sxs-lookup"><span data-stu-id="6810c-120">Requirement</span></span> | <span data-ttu-id="6810c-121">值</span><span class="sxs-lookup"><span data-stu-id="6810c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6810c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6810c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6810c-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="6810c-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6810c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6810c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6810c-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6810c-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6810c-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="6810c-126">Namespace</span></span><br/>                | <span data-ttu-id="6810c-127">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="6810c-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6810c-128">MOF</span><span class="sxs-lookup"><span data-stu-id="6810c-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6810c-129"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="6810c-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6810c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6810c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6810c-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6810c-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6810c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6810c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6810c-133">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="6810c-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





