---
title: IMsTscSecuredSettings WorkDir 屬性
description: 指定啟動程式的工作目錄。
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- WorkDir 屬性遠端桌面服務
- WorkDir 屬性遠端桌面服務，IMsTscSecuredSettings 介面
- IMsTscSecuredSettings 介面遠端桌面服務，WorkDir 屬性
- WorkDir 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，WorkDir 屬性
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966351"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="3159a-108">IMsTscSecuredSettings：： WorkDir 屬性</span><span class="sxs-lookup"><span data-stu-id="3159a-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="3159a-109">指定啟動程式的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="3159a-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="3159a-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3159a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3159a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3159a-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="3159a-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3159a-112">Property value</span></span>

<span data-ttu-id="3159a-113">新的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="3159a-113">The new working directory.</span></span> <span data-ttu-id="3159a-114">這個字串的最大長度為 **最大 \_ 路徑**-1 個字元。</span><span class="sxs-lookup"><span data-stu-id="3159a-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3159a-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="3159a-115">Error codes</span></span>

<span data-ttu-id="3159a-116">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="3159a-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3159a-117">備註</span><span class="sxs-lookup"><span data-stu-id="3159a-117">Remarks</span></span>

<span data-ttu-id="3159a-118">如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。</span><span class="sxs-lookup"><span data-stu-id="3159a-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="3159a-119">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="3159a-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3159a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3159a-120">Requirements</span></span>



| <span data-ttu-id="3159a-121">需求</span><span class="sxs-lookup"><span data-stu-id="3159a-121">Requirement</span></span> | <span data-ttu-id="3159a-122">值</span><span class="sxs-lookup"><span data-stu-id="3159a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3159a-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3159a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3159a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3159a-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3159a-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3159a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3159a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3159a-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3159a-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3159a-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="3159a-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3159a-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="3159a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3159a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3159a-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3159a-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="3159a-131">IID</span><span class="sxs-lookup"><span data-stu-id="3159a-131">IID</span></span><br/>                      | <span data-ttu-id="3159a-132">IID \_ IMsTscSecuredSettings 定義為 c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="3159a-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3159a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3159a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3159a-134">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="3159a-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="3159a-135">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="3159a-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





