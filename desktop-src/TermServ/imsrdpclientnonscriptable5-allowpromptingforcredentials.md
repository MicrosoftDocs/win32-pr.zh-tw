---
title: IMsRdpClientNonScriptable5 AllowPromptingForCredentials 屬性
description: 指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- AllowPromptingForCredentials 屬性遠端桌面服務
- AllowPromptingForCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，AllowPromptingForCredentials 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965953"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="93a83-106">IMsRdpClientNonScriptable5：： AllowPromptingForCredentials 屬性</span><span class="sxs-lookup"><span data-stu-id="93a83-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="93a83-107">指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="93a83-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="93a83-108">如果此屬性包含 **VARIANT \_ TRUE**，就會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="93a83-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="93a83-109">如果此屬性包含 **VARIANT \_ FALSE**，則不會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="93a83-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="93a83-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="93a83-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a83-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="93a83-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="93a83-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="93a83-112">Property value</span></span>

<span data-ttu-id="93a83-113">指定新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="93a83-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a83-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="93a83-114">Requirements</span></span>



| <span data-ttu-id="93a83-115">需求</span><span class="sxs-lookup"><span data-stu-id="93a83-115">Requirement</span></span> | <span data-ttu-id="93a83-116">值</span><span class="sxs-lookup"><span data-stu-id="93a83-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a83-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93a83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="93a83-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93a83-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="93a83-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93a83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="93a83-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="93a83-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="93a83-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="93a83-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="93a83-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93a83-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="93a83-123">DLL</span><span class="sxs-lookup"><span data-stu-id="93a83-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a83-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93a83-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="93a83-125">IID</span><span class="sxs-lookup"><span data-stu-id="93a83-125">IID</span></span><br/>                      | <span data-ttu-id="93a83-126">IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="93a83-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93a83-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93a83-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a83-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="93a83-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





