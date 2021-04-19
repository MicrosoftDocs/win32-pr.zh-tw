---
title: IMsRdpClientShell2 SecuredSettingsEnabled 屬性
description: 抓取值，指出目前的網頁是否位於信任的 Internet Explorer URL 安全性區域中。
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- SecuredSettingsEnabled 屬性遠端桌面服務
- SecuredSettingsEnabled 屬性遠端桌面服務，IMsRdpClientShell2 介面
- IMsRdpClientShell2 介面遠端桌面服務，SecuredSettingsEnabled 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968594"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="59c98-106">IMsRdpClientShell2：： SecuredSettingsEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="59c98-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="59c98-107">抓取值，指出目前的網頁是否位於信任的 Internet Explorer URL 安全性區域中。</span><span class="sxs-lookup"><span data-stu-id="59c98-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="59c98-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="59c98-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59c98-109">語法</span><span class="sxs-lookup"><span data-stu-id="59c98-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="59c98-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="59c98-110">Property value</span></span>

<span data-ttu-id="59c98-111">布林值的指標，指出目前網頁是否位於信任的 Internet Explorer URL 安全性區域中。</span><span class="sxs-lookup"><span data-stu-id="59c98-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c98-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="59c98-112">Requirements</span></span>



| <span data-ttu-id="59c98-113">需求</span><span class="sxs-lookup"><span data-stu-id="59c98-113">Requirement</span></span> | <span data-ttu-id="59c98-114">值</span><span class="sxs-lookup"><span data-stu-id="59c98-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c98-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59c98-115">Minimum supported client</span></span><br/> | <span data-ttu-id="59c98-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59c98-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59c98-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59c98-117">Minimum supported server</span></span><br/> | <span data-ttu-id="59c98-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59c98-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="59c98-119">DLL</span><span class="sxs-lookup"><span data-stu-id="59c98-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c98-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59c98-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c98-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59c98-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c98-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="59c98-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





