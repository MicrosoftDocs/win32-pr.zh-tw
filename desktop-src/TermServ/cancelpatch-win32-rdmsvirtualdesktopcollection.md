---
title: Win32_RDMSVirtualDesktopCollection 類別的 CancelPatch 方法
description: 取消虛擬機器集合中虛擬機器的軟體更新布建作業。
ms.assetid: fb0d6831-5c69-4017-b725-1a5038ad69f5
ms.tgt_platform: multiple
keywords:
- CancelPatch 方法遠端桌面服務
- CancelPatch 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，CancelPatch 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.CancelPatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56f33a819da976187fba823ac30fada9ff38730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967320"
---
# <a name="cancelpatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="b6508-106">Win32 RDMSVirtualDesktopCollection 類別的 CancelPatch 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b6508-106">CancelPatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="b6508-107">取消虛擬機器集合中虛擬機器的軟體更新布建作業。</span><span class="sxs-lookup"><span data-stu-id="b6508-107">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6508-108">語法</span><span class="sxs-lookup"><span data-stu-id="b6508-108">Syntax</span></span>


```mof
uint32 CancelPatch();
```



## <a name="parameters"></a><span data-ttu-id="b6508-109">參數</span><span class="sxs-lookup"><span data-stu-id="b6508-109">Parameters</span></span>

<span data-ttu-id="b6508-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b6508-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6508-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6508-111">Return value</span></span>

<span data-ttu-id="b6508-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b6508-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6508-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6508-113">Requirements</span></span>



| <span data-ttu-id="b6508-114">需求</span><span class="sxs-lookup"><span data-stu-id="b6508-114">Requirement</span></span> | <span data-ttu-id="b6508-115">值</span><span class="sxs-lookup"><span data-stu-id="b6508-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6508-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6508-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6508-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="b6508-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b6508-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6508-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6508-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6508-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b6508-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="b6508-120">Namespace</span></span><br/>                | <span data-ttu-id="b6508-121">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="b6508-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b6508-122">MOF</span><span class="sxs-lookup"><span data-stu-id="b6508-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6508-123"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6508-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6508-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b6508-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6508-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6508-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b6508-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6508-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6508-127">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="b6508-127">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





