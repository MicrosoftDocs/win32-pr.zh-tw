---
title: IMsTscSecuredSettings 全螢幕屬性
description: 指定用戶端控制項的全螢幕狀態。
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- 全螢幕屬性遠端桌面服務
- 全螢幕屬性遠端桌面服務、IMsTscSecuredSettings 介面
- IMsTscSecuredSettings 介面遠端桌面服務、全螢幕屬性
- 全螢幕屬性遠端桌面服務、IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務、全螢幕屬性
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965522"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="63b4f-108">IMsTscSecuredSettings：：全螢幕屬性</span><span class="sxs-lookup"><span data-stu-id="63b4f-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="63b4f-109">指定用戶端控制項的全螢幕狀態。</span><span class="sxs-lookup"><span data-stu-id="63b4f-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="63b4f-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="63b4f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b4f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="63b4f-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="63b4f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="63b4f-112">Property value</span></span>

<span data-ttu-id="63b4f-113">如果控制項應使用全螢幕模式，請將此參數設定為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="63b4f-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63b4f-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="63b4f-114">Error codes</span></span>

<span data-ttu-id="63b4f-115">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="63b4f-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="63b4f-116">備註</span><span class="sxs-lookup"><span data-stu-id="63b4f-116">Remarks</span></span>

<span data-ttu-id="63b4f-117">如需此方法的詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md)。</span><span class="sxs-lookup"><span data-stu-id="63b4f-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="63b4f-118">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="63b4f-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="63b4f-119">請注意，雖然使用此屬性只限于允許的 Internet Explorer URL 安全性區域，但是在建立連線之後，使用者隨時都可以在建立連線之後變更為全 [螢幕模式 (](terminal-services-shortcut-keys.md) CTRL + ALT + BREAK) 。</span><span class="sxs-lookup"><span data-stu-id="63b4f-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="63b4f-120">建立用戶端連接時，可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="63b4f-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="63b4f-121">您必須先呼叫 [**IMsRdpClientNonScriptable3：:p 的 \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) 方法，然後再呼叫 **IMsTscSecuredSettings：:p 的 \_ 全像全螢幕** 方法或 [**IMsRdpClient：:p 的 ui \_ 全螢幕**](imsrdpclient-fullscreen.md) 方式。</span><span class="sxs-lookup"><span data-stu-id="63b4f-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63b4f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="63b4f-122">Requirements</span></span>



| <span data-ttu-id="63b4f-123">需求</span><span class="sxs-lookup"><span data-stu-id="63b4f-123">Requirement</span></span> | <span data-ttu-id="63b4f-124">值</span><span class="sxs-lookup"><span data-stu-id="63b4f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b4f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63b4f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63b4f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63b4f-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="63b4f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63b4f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63b4f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63b4f-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="63b4f-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="63b4f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="63b4f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b4f-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="63b4f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="63b4f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63b4f-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b4f-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="63b4f-133">IID</span><span class="sxs-lookup"><span data-stu-id="63b4f-133">IID</span></span><br/>                      | <span data-ttu-id="63b4f-134">IID \_ IMsTscSecuredSettings 定義為 c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="63b4f-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63b4f-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63b4f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b4f-136">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="63b4f-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="63b4f-137">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="63b4f-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





