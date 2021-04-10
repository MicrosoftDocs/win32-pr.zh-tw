---
title: IMsRdpClientShell2 MsRdpWorkspace 屬性
description: 抓取 IMsRdpWorkspace 介面的指標，該介面可用來管理 RemoteApp 和桌面連線的認證和連接。
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- MsRdpWorkspace 屬性遠端桌面服務
- MsRdpWorkspace 屬性遠端桌面服務，IMsRdpClientShell2 介面
- IMsRdpClientShell2 介面遠端桌面服務，MsRdpWorkspace 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686132"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="c81c0-106">IMsRdpClientShell2：： MsRdpWorkspace 屬性</span><span class="sxs-lookup"><span data-stu-id="c81c0-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="c81c0-107">抓取 [**IMsRdpWorkspace**](imsrdpworkspace.md) 介面的指標，該介面可用來管理 RemoteApp 和桌面連線的認證和連接。</span><span class="sxs-lookup"><span data-stu-id="c81c0-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="c81c0-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c81c0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c81c0-109">語法</span><span class="sxs-lookup"><span data-stu-id="c81c0-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="c81c0-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="c81c0-110">Property value</span></span>

<span data-ttu-id="c81c0-111">[**IMsRdpWorkspace**](imsrdpworkspace.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c81c0-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c81c0-112">備註</span><span class="sxs-lookup"><span data-stu-id="c81c0-112">Remarks</span></span>

<span data-ttu-id="c81c0-113">[**IMsRdpWorkspace**](imsrdpworkspace.md)介面不會公開為自訂介面。</span><span class="sxs-lookup"><span data-stu-id="c81c0-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="c81c0-114">它只能透過 [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) 方法來存取。</span><span class="sxs-lookup"><span data-stu-id="c81c0-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81c0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c81c0-115">Requirements</span></span>



| <span data-ttu-id="c81c0-116">需求</span><span class="sxs-lookup"><span data-stu-id="c81c0-116">Requirement</span></span> | <span data-ttu-id="c81c0-117">值</span><span class="sxs-lookup"><span data-stu-id="c81c0-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c81c0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c81c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c81c0-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c81c0-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c81c0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c81c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c81c0-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c81c0-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="c81c0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c81c0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c81c0-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c81c0-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81c0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c81c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81c0-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="c81c0-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

