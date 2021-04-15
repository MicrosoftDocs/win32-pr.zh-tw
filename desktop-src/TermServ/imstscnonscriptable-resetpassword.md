---
title: IMsTscNonScriptable ResetPassword 方法
description: 重設遠端桌面 ActiveX 控制項中的所有密碼狀態。
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- ResetPassword 方法遠端桌面服務
- ResetPassword 方法遠端桌面服務，IMsTscNonScriptable 介面
- IMsTscNonScriptable 介面遠端桌面服務，ResetPassword 方法
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466752"
---
# <a name="imstscnonscriptableresetpassword-method"></a><span data-ttu-id="2adea-106">IMsTscNonScriptable：： ResetPassword 方法</span><span class="sxs-lookup"><span data-stu-id="2adea-106">IMsTscNonScriptable::ResetPassword method</span></span>

<span data-ttu-id="2adea-107">重設遠端桌面 ActiveX 控制項中的所有密碼狀態。</span><span class="sxs-lookup"><span data-stu-id="2adea-107">Resets all password states in the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="2adea-108">您可以呼叫這個方法，以清除以下列三種支援格式之一儲存的密碼：純文字、可攜的編碼或二進位 (nonportable) 編碼。</span><span class="sxs-lookup"><span data-stu-id="2adea-108">You can call this method to clear passwords that are stored in any one of the three supported formats: plaintext, portable encoded, or binary (nonportable) encoded.</span></span> <span data-ttu-id="2adea-109">請注意，編碼的密碼不應被安全地加密。</span><span class="sxs-lookup"><span data-stu-id="2adea-109">Note that encoded passwords should not be considered securely encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="2adea-110">語法</span><span class="sxs-lookup"><span data-stu-id="2adea-110">Syntax</span></span>


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a><span data-ttu-id="2adea-111">參數</span><span class="sxs-lookup"><span data-stu-id="2adea-111">Parameters</span></span>

<span data-ttu-id="2adea-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2adea-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2adea-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2adea-113">Return value</span></span>

<span data-ttu-id="2adea-114">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="2adea-114">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2adea-115">備註</span><span class="sxs-lookup"><span data-stu-id="2adea-115">Remarks</span></span>

<span data-ttu-id="2adea-116">您可以呼叫這個方法，在中斷連接之後重設控制項的密碼。</span><span class="sxs-lookup"><span data-stu-id="2adea-116">You can call this method to reset the control's password after disconnecting.</span></span> <span data-ttu-id="2adea-117">這樣可確保使用相同控制項實例的後續連接不會自動以先前設定的密碼登入。</span><span class="sxs-lookup"><span data-stu-id="2adea-117">This ensures that subsequent connections that use the same instance of the control do not automatically log on with a previously set password.</span></span>

<span data-ttu-id="2adea-118">只有當遠端桌面 ActiveX 控制項不是處於線上狀態時，您才能呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="2adea-118">You can only call this method when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="2adea-119">如果在連接控制項時呼叫，這個方法 **會傳回 E \_ FAIL** 。</span><span class="sxs-lookup"><span data-stu-id="2adea-119">This method returns **E\_FAIL** if called when the control is connected.</span></span> <span data-ttu-id="2adea-120">若要檢查連接狀態，請透過 [**IMsTscAx**](imstscax-interface.md)介面或繼承自它的其中一個介面，呼叫 [**get \_ connected**](imstscax-connected.md)方法。</span><span class="sxs-lookup"><span data-stu-id="2adea-120">To check for the connected state, call the [**get\_Connected**](imstscax-connected.md) method through the [**IMsTscAx**](imstscax-interface.md) interface or one of the interfaces that inherits from it.</span></span>

<span data-ttu-id="2adea-121">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2adea-121">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2adea-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2adea-122">Requirements</span></span>



| <span data-ttu-id="2adea-123">需求</span><span class="sxs-lookup"><span data-stu-id="2adea-123">Requirement</span></span> | <span data-ttu-id="2adea-124">值</span><span class="sxs-lookup"><span data-stu-id="2adea-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2adea-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2adea-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2adea-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2adea-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2adea-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2adea-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2adea-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2adea-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2adea-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2adea-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="2adea-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2adea-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2adea-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2adea-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2adea-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2adea-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2adea-133">IID</span><span class="sxs-lookup"><span data-stu-id="2adea-133">IID</span></span><br/>                      | <span data-ttu-id="2adea-134">IID \_ IMsTscNonScriptable 定義為 c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="2adea-134">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2adea-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2adea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2adea-136">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="2adea-136">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





