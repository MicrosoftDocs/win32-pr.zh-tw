---
title: IMsRdpClientShell PublicMode 屬性
description: 指定或抓取是否啟用公用模式。
ms.assetid: 983d3e46-f09e-4425-88a1-9d4ae0d9c70a
ms.tgt_platform: multiple
keywords:
- PublicMode 屬性遠端桌面服務
- PublicMode 屬性遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，PublicMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell.PublicMode
- IMsRdpClientShell.get_PublicMode
- IMsRdpClientShell.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4129b3a9eeb62af0fa6e970c812ea6adf9670c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466004"
---
# <a name="imsrdpclientshellpublicmode-property"></a><span data-ttu-id="6e61f-106">IMsRdpClientShell：:P ublicMode 屬性</span><span class="sxs-lookup"><span data-stu-id="6e61f-106">IMsRdpClientShell::PublicMode property</span></span>

<span data-ttu-id="6e61f-107">指定或抓取是否啟用公用模式。</span><span class="sxs-lookup"><span data-stu-id="6e61f-107">Specifies or retrieves whether public mode is enabled.</span></span>

<span data-ttu-id="6e61f-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6e61f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e61f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e61f-109">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="6e61f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6e61f-110">Property value</span></span>

<span data-ttu-id="6e61f-111">指定是否啟用公用模式。</span><span class="sxs-lookup"><span data-stu-id="6e61f-111">Specifies whether public mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e61f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e61f-112">Requirements</span></span>



| <span data-ttu-id="6e61f-113">需求</span><span class="sxs-lookup"><span data-stu-id="6e61f-113">Requirement</span></span> | <span data-ttu-id="6e61f-114">值</span><span class="sxs-lookup"><span data-stu-id="6e61f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e61f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e61f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6e61f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e61f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6e61f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e61f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6e61f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e61f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6e61f-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6e61f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e61f-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e61f-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e61f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6e61f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e61f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e61f-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e61f-123">IID</span><span class="sxs-lookup"><span data-stu-id="6e61f-123">IID</span></span><br/>                      | <span data-ttu-id="6e61f-124">IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="6e61f-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="6e61f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e61f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e61f-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="6e61f-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





