---
title: IMsRdpClientSecuredSettings AudioRedirectionMode 屬性
description: 指定音訊重新導向設定，指定是否要在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上，重新導向聲音或播放音效。
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- AudioRedirectionMode 屬性遠端桌面服務
- AudioRedirectionMode 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，AudioRedirectionMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509469"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="3b735-106">IMsRdpClientSecuredSettings：： AudioRedirectionMode 屬性</span><span class="sxs-lookup"><span data-stu-id="3b735-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="3b735-107">指定音訊重新導向設定，指定是否要在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上，重新導向聲音或播放音效。</span><span class="sxs-lookup"><span data-stu-id="3b735-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="3b735-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b735-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b735-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b735-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="3b735-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="3b735-110">Property value</span></span>

<span data-ttu-id="3b735-111">新的設定。</span><span class="sxs-lookup"><span data-stu-id="3b735-111">The new settings.</span></span> <span data-ttu-id="3b735-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3b735-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="3b735-113">0</span><span class="sxs-lookup"><span data-stu-id="3b735-113">0</span></span>
</dt> <dd>

<span data-ttu-id="3b735-114">將聲音重新導向至用戶端。</span><span class="sxs-lookup"><span data-stu-id="3b735-114">Redirect sounds to the client.</span></span> <span data-ttu-id="3b735-115">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="3b735-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="3b735-116">1</span><span class="sxs-lookup"><span data-stu-id="3b735-116">1</span></span>
</dt> <dd>

<span data-ttu-id="3b735-117">在遠端電腦上播放音效。</span><span class="sxs-lookup"><span data-stu-id="3b735-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="3b735-118">2</span><span class="sxs-lookup"><span data-stu-id="3b735-118">2</span></span>
</dt> <dd>

<span data-ttu-id="3b735-119">停用音效重新導向;不要在伺服器上播放聲音。</span><span class="sxs-lookup"><span data-stu-id="3b735-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="3b735-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3b735-120">Error codes</span></span>

<span data-ttu-id="3b735-121">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="3b735-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b735-122">備註</span><span class="sxs-lookup"><span data-stu-id="3b735-122">Remarks</span></span>

<span data-ttu-id="3b735-123">連接控制項時無法設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b735-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="3b735-124">如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。</span><span class="sxs-lookup"><span data-stu-id="3b735-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="3b735-125">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="3b735-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b735-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b735-126">Requirements</span></span>



| <span data-ttu-id="3b735-127">需求</span><span class="sxs-lookup"><span data-stu-id="3b735-127">Requirement</span></span> | <span data-ttu-id="3b735-128">值</span><span class="sxs-lookup"><span data-stu-id="3b735-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b735-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b735-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b735-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b735-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="3b735-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b735-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b735-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b735-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="3b735-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3b735-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b735-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b735-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="3b735-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3b735-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b735-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b735-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="3b735-137">IID</span><span class="sxs-lookup"><span data-stu-id="3b735-137">IID</span></span><br/>                      | <span data-ttu-id="3b735-138">IID \_ IMsRdpClientSecuredSettings 定義為605befcf-39c1-45cc-a811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="3b735-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b735-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b735-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b735-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="3b735-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





