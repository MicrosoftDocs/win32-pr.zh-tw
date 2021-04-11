---
title: Win32_VirtualDesktopSession 類別的中斷連接方法
description: 中斷虛擬桌面會話的連線。
ms.assetid: 9dbb256c-c416-4749-87be-05a906070560
ms.tgt_platform: multiple
keywords:
- 中斷連接方法遠端桌面服務
- 中斷連接方法遠端桌面服務，Win32_VirtualDesktopSession 類別
- Win32_VirtualDesktopSession 類別遠端桌面服務，中斷連線方法
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Disconnect
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d473286dec0d286b0e5e9e310c146bd46a2f95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384905"
---
# <a name="disconnect-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="7d8c5-106">Win32 VirtualDesktopSession 類別的 Disconnect 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7d8c5-106">Disconnect method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="7d8c5-107">中斷虛擬桌面會話的連線。</span><span class="sxs-lookup"><span data-stu-id="7d8c5-107">Disconnects the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8c5-108">語法</span><span class="sxs-lookup"><span data-stu-id="7d8c5-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="7d8c5-109">參數</span><span class="sxs-lookup"><span data-stu-id="7d8c5-109">Parameters</span></span>

<span data-ttu-id="7d8c5-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d8c5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d8c5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d8c5-111">Return value</span></span>

<span data-ttu-id="7d8c5-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7d8c5-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8c5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d8c5-113">Requirements</span></span>



| <span data-ttu-id="7d8c5-114">需求</span><span class="sxs-lookup"><span data-stu-id="7d8c5-114">Requirement</span></span> | <span data-ttu-id="7d8c5-115">值</span><span class="sxs-lookup"><span data-stu-id="7d8c5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8c5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d8c5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8c5-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="7d8c5-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7d8c5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d8c5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8c5-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d8c5-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7d8c5-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d8c5-120">Namespace</span></span><br/>                | <span data-ttu-id="7d8c5-121">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="7d8c5-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7d8c5-122">MOF</span><span class="sxs-lookup"><span data-stu-id="7d8c5-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d8c5-123"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d8c5-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d8c5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7d8c5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d8c5-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d8c5-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7d8c5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d8c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8c5-127">**Win32 \_ VirtualDesktopSession**</span><span class="sxs-lookup"><span data-stu-id="7d8c5-127">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





