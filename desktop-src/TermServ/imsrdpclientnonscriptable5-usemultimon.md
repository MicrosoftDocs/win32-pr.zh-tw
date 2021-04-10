---
title: IMsRdpClientNonScriptable5 UseMultimon 屬性
description: 指定遠端桌面 ActiveX 控制項是否應該使用多個監視器。
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- UseMultimon 屬性遠端桌面服務
- UseMultimon 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，UseMultimon 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934664"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="20b33-106">IMsRdpClientNonScriptable5：： UseMultimon 屬性</span><span class="sxs-lookup"><span data-stu-id="20b33-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="20b33-107">指定遠端桌面 ActiveX 控制項是否應該使用多個監視器。</span><span class="sxs-lookup"><span data-stu-id="20b33-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="20b33-108">如果這個屬性包含 **VARIANT \_ TRUE**，控制項將會使用多個監視器。</span><span class="sxs-lookup"><span data-stu-id="20b33-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="20b33-109">如果這個屬性包含 **VARIANT \_ FALSE**，控制項就不會使用多個監視器。</span><span class="sxs-lookup"><span data-stu-id="20b33-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="20b33-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="20b33-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b33-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="20b33-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="20b33-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="20b33-112">Property value</span></span>

<span data-ttu-id="20b33-113">指定新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="20b33-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b33-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="20b33-114">Requirements</span></span>



| <span data-ttu-id="20b33-115">需求</span><span class="sxs-lookup"><span data-stu-id="20b33-115">Requirement</span></span> | <span data-ttu-id="20b33-116">值</span><span class="sxs-lookup"><span data-stu-id="20b33-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b33-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20b33-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20b33-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20b33-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="20b33-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20b33-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20b33-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="20b33-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="20b33-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="20b33-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="20b33-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b33-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="20b33-123">DLL</span><span class="sxs-lookup"><span data-stu-id="20b33-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b33-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b33-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="20b33-125">IID</span><span class="sxs-lookup"><span data-stu-id="20b33-125">IID</span></span><br/>                      | <span data-ttu-id="20b33-126">IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="20b33-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20b33-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20b33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b33-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="20b33-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





