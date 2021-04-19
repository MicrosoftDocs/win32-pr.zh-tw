---
description: 停用網路介面卡。
ms.assetid: 6b328d7c-a9ef-4c9b-bc32-13fa2e0f65eb
ms.tgt_platform: multiple
title: Disable Win32_NetworkAdapter 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a9c6b1a506310460d9131709092b739f68986e02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972128"
---
# <a name="disable-method-of-the-win32_networkadapter-class"></a><span data-ttu-id="cde18-103">Disable Win32 \_ NetworkAdapter 類別的方法</span><span class="sxs-lookup"><span data-stu-id="cde18-103">Disable method of the Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="cde18-104">**Disable** 方法會停用網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="cde18-104">The **Disable** method disables the network adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde18-105">語法</span><span class="sxs-lookup"><span data-stu-id="cde18-105">Syntax</span></span>


```mof
uint32 Disable();
```



## <a name="parameters"></a><span data-ttu-id="cde18-106">參數</span><span class="sxs-lookup"><span data-stu-id="cde18-106">Parameters</span></span>

<span data-ttu-id="cde18-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cde18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cde18-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="cde18-108">Return value</span></span>

<span data-ttu-id="cde18-109">傳回零 (0) 表示成功。</span><span class="sxs-lookup"><span data-stu-id="cde18-109">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="cde18-110">任何其他數字表示發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="cde18-110">Any other number indicates an error.</span></span> <span data-ttu-id="cde18-111">如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="cde18-111">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="cde18-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cde18-112">Requirements</span></span>



| <span data-ttu-id="cde18-113">需求</span><span class="sxs-lookup"><span data-stu-id="cde18-113">Requirement</span></span> | <span data-ttu-id="cde18-114">值</span><span class="sxs-lookup"><span data-stu-id="cde18-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde18-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cde18-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cde18-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cde18-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cde18-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cde18-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cde18-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cde18-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cde18-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="cde18-119">Namespace</span></span><br/>                | <span data-ttu-id="cde18-120">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cde18-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cde18-121">MOF</span><span class="sxs-lookup"><span data-stu-id="cde18-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde18-122"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cde18-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde18-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cde18-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde18-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde18-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde18-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cde18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde18-126">**Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="cde18-126">**Win32\_NetworkAdapter**</span></span>](win32-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="cde18-127">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="cde18-127">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="cde18-128">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="cde18-128">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

