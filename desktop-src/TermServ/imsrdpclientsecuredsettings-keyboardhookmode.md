---
title: IMsRdpClientSecuredSettings KeyboardHookMode 屬性
description: 指定鍵盤重新導向設定，以指定套用 Windows 鍵盤快捷方式的方式和時機 (例如，ALT + TAB) 。
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- KeyboardHookMode 屬性遠端桌面服務
- KeyboardHookMode 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，KeyboardHookMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384294"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a><span data-ttu-id="12e24-106">IMsRdpClientSecuredSettings：： KeyboardHookMode 屬性</span><span class="sxs-lookup"><span data-stu-id="12e24-106">IMsRdpClientSecuredSettings::KeyboardHookMode property</span></span>

<span data-ttu-id="12e24-107">指定鍵盤重新導向設定，以指定套用 Windows 鍵盤快捷方式的方式和時機 (例如，ALT + TAB) 。</span><span class="sxs-lookup"><span data-stu-id="12e24-107">Specifies the keyboard redirection settings, which specify how and when to apply Windows keyboard shortcut (for example, ALT+TAB).</span></span>

<span data-ttu-id="12e24-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="12e24-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e24-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e24-109">Syntax</span></span>


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a><span data-ttu-id="12e24-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="12e24-110">Property value</span></span>

<span data-ttu-id="12e24-111">新的設定。</span><span class="sxs-lookup"><span data-stu-id="12e24-111">The new settings.</span></span> <span data-ttu-id="12e24-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="12e24-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="12e24-113">0</span><span class="sxs-lookup"><span data-stu-id="12e24-113">0</span></span>
</dt> <dd>

<span data-ttu-id="12e24-114">只將金鑰組合套用到用戶端電腦的本機。</span><span class="sxs-lookup"><span data-stu-id="12e24-114">Apply key combinations only locally at the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="12e24-115">1</span><span class="sxs-lookup"><span data-stu-id="12e24-115">1</span></span>
</dt> <dd>

<span data-ttu-id="12e24-116">將金鑰組合套用到遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="12e24-116">Apply key combinations at the remote server.</span></span>

</dd> <dt>

<span data-ttu-id="12e24-117">2</span><span class="sxs-lookup"><span data-stu-id="12e24-117">2</span></span>
</dt> <dd>

<span data-ttu-id="12e24-118">只有在用戶端以全螢幕模式執行時，才將金鑰組合套用至遠端伺服器。</span><span class="sxs-lookup"><span data-stu-id="12e24-118">Apply key combinations to the remote server only when the client is running in full-screen mode.</span></span> <span data-ttu-id="12e24-119">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="12e24-119">This is the default value.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="12e24-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="12e24-120">Error codes</span></span>

<span data-ttu-id="12e24-121">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="12e24-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e24-122">備註</span><span class="sxs-lookup"><span data-stu-id="12e24-122">Remarks</span></span>

<span data-ttu-id="12e24-123">連接控制項時無法設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="12e24-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="12e24-124">如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。</span><span class="sxs-lookup"><span data-stu-id="12e24-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="12e24-125">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="12e24-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12e24-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="12e24-126">Requirements</span></span>



| <span data-ttu-id="12e24-127">需求</span><span class="sxs-lookup"><span data-stu-id="12e24-127">Requirement</span></span> | <span data-ttu-id="12e24-128">值</span><span class="sxs-lookup"><span data-stu-id="12e24-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e24-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12e24-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12e24-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12e24-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="12e24-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12e24-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12e24-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12e24-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="12e24-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="12e24-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="12e24-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e24-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="12e24-135">DLL</span><span class="sxs-lookup"><span data-stu-id="12e24-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e24-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e24-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="12e24-137">IID</span><span class="sxs-lookup"><span data-stu-id="12e24-137">IID</span></span><br/>                      | <span data-ttu-id="12e24-138">IID \_ IMsRdpClientSecuredSettings 定義為605befcf-39c1-45cc-a811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="12e24-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12e24-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e24-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e24-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="12e24-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





