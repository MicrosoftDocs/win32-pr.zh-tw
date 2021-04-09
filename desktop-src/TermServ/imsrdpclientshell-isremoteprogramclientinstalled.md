---
title: IMsRdpClientShell IsRemoteProgramClientInstalled 屬性
description: 抓取遠端桌面連線 (RDC) 用戶端是否支援 Windows Server 2008 R2 RemoteApp 功能。
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- IsRemoteProgramClientInstalled 屬性遠端桌面服務
- IsRemoteProgramClientInstalled 屬性遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，IsRemoteProgramClientInstalled 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094219"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="7d9aa-106">IMsRdpClientShell：： IsRemoteProgramClientInstalled 屬性</span><span class="sxs-lookup"><span data-stu-id="7d9aa-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="7d9aa-107">抓取遠端桌面連線 (RDC) 用戶端是否支援 Windows Server 2008 R2 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="7d9aa-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="7d9aa-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7d9aa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d9aa-109">語法</span><span class="sxs-lookup"><span data-stu-id="7d9aa-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="7d9aa-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="7d9aa-110">Property value</span></span>

<span data-ttu-id="7d9aa-111">抓取遠端桌面連線 (RDC) 用戶端是否支援 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="7d9aa-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9aa-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d9aa-112">Requirements</span></span>



| <span data-ttu-id="7d9aa-113">需求</span><span class="sxs-lookup"><span data-stu-id="7d9aa-113">Requirement</span></span> | <span data-ttu-id="7d9aa-114">值</span><span class="sxs-lookup"><span data-stu-id="7d9aa-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9aa-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d9aa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7d9aa-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d9aa-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7d9aa-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d9aa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7d9aa-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d9aa-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7d9aa-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7d9aa-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d9aa-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d9aa-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d9aa-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7d9aa-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d9aa-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d9aa-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d9aa-123">IID</span><span class="sxs-lookup"><span data-stu-id="7d9aa-123">IID</span></span><br/>                      | <span data-ttu-id="7d9aa-124">IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="7d9aa-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7d9aa-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d9aa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9aa-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="7d9aa-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





