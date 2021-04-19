---
title: IMsTscSecuredSettings StartProgram 屬性
description: 指定連接時要在遠端伺服器上啟動的程式。
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- StartProgram 屬性遠端桌面服務
- StartProgram 屬性遠端桌面服務，IMsTscSecuredSettings 介面
- IMsTscSecuredSettings 介面遠端桌面服務，StartProgram 屬性
- StartProgram 屬性遠端桌面服務，IMsRdpClientSecuredSettings 介面
- IMsRdpClientSecuredSettings 介面遠端桌面服務，StartProgram 屬性
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966352"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="2bdd2-108">IMsTscSecuredSettings：： StartProgram 屬性</span><span class="sxs-lookup"><span data-stu-id="2bdd2-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="2bdd2-109">指定連接時要在遠端伺服器上啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="2bdd2-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdd2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bdd2-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="2bdd2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="2bdd2-112">Property value</span></span>

<span data-ttu-id="2bdd2-113">新啟動程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-113">The name of the new start program.</span></span> <span data-ttu-id="2bdd2-114">這個字串的最大長度為 **最大 \_ 路徑**-1 個字元。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2bdd2-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2bdd2-115">Error codes</span></span>

<span data-ttu-id="2bdd2-116">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bdd2-117">備註</span><span class="sxs-lookup"><span data-stu-id="2bdd2-117">Remarks</span></span>

<span data-ttu-id="2bdd2-118">如果未設定這個屬性的值，則會執行會話使用者的 shell 命令。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="2bdd2-119">系統會從伺服器上的下列登錄值讀取 shell 命令：</span><span class="sxs-lookup"><span data-stu-id="2bdd2-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="2bdd2-120">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **Shell**</span><span class="sxs-lookup"><span data-stu-id="2bdd2-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="2bdd2-121">如需詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="2bdd2-122">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="2bdd2-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bdd2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bdd2-123">Requirements</span></span>



| <span data-ttu-id="2bdd2-124">需求</span><span class="sxs-lookup"><span data-stu-id="2bdd2-124">Requirement</span></span> | <span data-ttu-id="2bdd2-125">值</span><span class="sxs-lookup"><span data-stu-id="2bdd2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdd2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bdd2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2bdd2-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bdd2-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2bdd2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bdd2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2bdd2-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bdd2-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2bdd2-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2bdd2-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="2bdd2-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bdd2-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2bdd2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2bdd2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bdd2-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bdd2-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2bdd2-134">IID</span><span class="sxs-lookup"><span data-stu-id="2bdd2-134">IID</span></span><br/>                      | <span data-ttu-id="2bdd2-135">IID \_ IMsTscSecuredSettings 定義為 c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="2bdd2-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bdd2-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bdd2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bdd2-137">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="2bdd2-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2bdd2-138">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="2bdd2-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





