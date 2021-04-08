---
title: IMsRdpPreferredRedirectionInfo UseRedirectionServerName 屬性
description: 取得和設定是否使用重新導向伺服器名稱。
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- UseRedirectionServerName 屬性遠端桌面服務
- UseRedirectionServerName 屬性遠端桌面服務，IMsRdpPreferredRedirectionInfo 介面
- IMsRdpPreferredRedirectionInfo 介面遠端桌面服務，UseRedirectionServerName 屬性
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685722"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="aa960-106">IMsRdpPreferredRedirectionInfo：： UseRedirectionServerName 屬性</span><span class="sxs-lookup"><span data-stu-id="aa960-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="aa960-107">取得和設定是否使用重新導向伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="aa960-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="aa960-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="aa960-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa960-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa960-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="aa960-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="aa960-110">Property value</span></span>

<span data-ttu-id="aa960-111">是否要使用重新導向伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="aa960-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa960-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa960-112">Requirements</span></span>



| <span data-ttu-id="aa960-113">需求</span><span class="sxs-lookup"><span data-stu-id="aa960-113">Requirement</span></span> | <span data-ttu-id="aa960-114">值</span><span class="sxs-lookup"><span data-stu-id="aa960-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa960-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa960-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aa960-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aa960-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="aa960-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa960-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aa960-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa960-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="aa960-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aa960-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa960-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa960-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="aa960-121">DLL</span><span class="sxs-lookup"><span data-stu-id="aa960-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa960-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa960-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="aa960-123">IID</span><span class="sxs-lookup"><span data-stu-id="aa960-123">IID</span></span><br/>                      | <span data-ttu-id="aa960-124">IID \_ IMsRdpPreferredRedirectionInfo 定義為 FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="aa960-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa960-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa960-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa960-126">**IMsRdpPreferredRedirectionInfo**</span><span class="sxs-lookup"><span data-stu-id="aa960-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





