---
title: IMsRdpClientNonScriptable5 DisableRemoteAppCapsCheck 屬性
description: 指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- DisableRemoteAppCapsCheck 屬性遠端桌面服務
- DisableRemoteAppCapsCheck 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，DisableRemoteAppCapsCheck 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467021"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="6842f-106">IMsRdpClientNonScriptable5：:D isableRemoteAppCapsCheck 屬性</span><span class="sxs-lookup"><span data-stu-id="6842f-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="6842f-107">指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="6842f-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="6842f-108">如果這個屬性包含 **VARIANT \_ TRUE**，控制項就不應該檢查伺服器的 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="6842f-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="6842f-109">如果這個屬性包含 **VARIANT \_ FALSE**，控制項可以檢查伺服器的 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="6842f-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="6842f-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6842f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6842f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="6842f-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="6842f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6842f-112">Property value</span></span>

<span data-ttu-id="6842f-113">指定新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6842f-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6842f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6842f-114">Requirements</span></span>



| <span data-ttu-id="6842f-115">需求</span><span class="sxs-lookup"><span data-stu-id="6842f-115">Requirement</span></span> | <span data-ttu-id="6842f-116">值</span><span class="sxs-lookup"><span data-stu-id="6842f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6842f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6842f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6842f-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6842f-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6842f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6842f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6842f-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6842f-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="6842f-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6842f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6842f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6842f-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6842f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6842f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6842f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6842f-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="6842f-125">IID</span><span class="sxs-lookup"><span data-stu-id="6842f-125">IID</span></span><br/>                      | <span data-ttu-id="6842f-126">IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="6842f-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6842f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6842f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6842f-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6842f-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





