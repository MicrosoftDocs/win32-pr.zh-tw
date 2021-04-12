---
title: Win32_SessionDirectoryVMMPlugin 類別的 SetName 方法
description: 設定外掛程式的名稱。
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- SetName 方法遠端桌面服務
- SetName 方法遠端桌面服務，Win32_SessionDirectoryVMMPlugin 類別
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，SetName 方法
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317243"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="b081d-106">Win32 SessionDirectoryVMMPlugin 類別的 SetName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b081d-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="b081d-107">設定外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b081d-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="b081d-108">語法</span><span class="sxs-lookup"><span data-stu-id="b081d-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="b081d-109">參數</span><span class="sxs-lookup"><span data-stu-id="b081d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b081d-110">*sName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b081d-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b081d-111">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b081d-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b081d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b081d-112">Return value</span></span>

<span data-ttu-id="b081d-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b081d-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b081d-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b081d-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b081d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b081d-115">Requirements</span></span>



| <span data-ttu-id="b081d-116">需求</span><span class="sxs-lookup"><span data-stu-id="b081d-116">Requirement</span></span> | <span data-ttu-id="b081d-117">值</span><span class="sxs-lookup"><span data-stu-id="b081d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b081d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b081d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b081d-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="b081d-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b081d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b081d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b081d-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b081d-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b081d-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="b081d-122">Namespace</span></span><br/>                | <span data-ttu-id="b081d-123">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b081d-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b081d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b081d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b081d-125"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="b081d-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b081d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b081d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b081d-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b081d-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b081d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b081d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b081d-129">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="b081d-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





