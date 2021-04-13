---
title: Win32_TSVirtualIP 類別的 SetProgramList 方法
description: 覆寫使用 IP 虛擬化的程式清單。
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- SetProgramList 方法遠端桌面服務
- SetProgramList 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SetProgramList 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508739"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="a26a5-106">Win32 TSVirtualIP 類別的 SetProgramList 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a26a5-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="a26a5-107">覆寫使用 IP 虛擬化的程式清單。</span><span class="sxs-lookup"><span data-stu-id="a26a5-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="a26a5-108">語法</span><span class="sxs-lookup"><span data-stu-id="a26a5-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="a26a5-109">參數</span><span class="sxs-lookup"><span data-stu-id="a26a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a26a5-110">*ProgramList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a26a5-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a26a5-111">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a26a5-111">Type: **string\[\]**</span></span>

<span data-ttu-id="a26a5-112">字串陣列，其中包含使用 IP 虛擬化之程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="a26a5-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a26a5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a26a5-113">Return value</span></span>

<span data-ttu-id="a26a5-114">類型： **unint32**</span><span class="sxs-lookup"><span data-stu-id="a26a5-114">Type: **unint32**</span></span>

<span data-ttu-id="a26a5-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a26a5-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a26a5-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="a26a5-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a26a5-117">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a26a5-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a26a5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a26a5-118">Requirements</span></span>



| <span data-ttu-id="a26a5-119">需求</span><span class="sxs-lookup"><span data-stu-id="a26a5-119">Requirement</span></span> | <span data-ttu-id="a26a5-120">值</span><span class="sxs-lookup"><span data-stu-id="a26a5-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a26a5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a26a5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a26a5-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="a26a5-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a26a5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a26a5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a26a5-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a26a5-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a26a5-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="a26a5-125">Namespace</span></span><br/>                | <span data-ttu-id="a26a5-126">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a26a5-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a26a5-127">MOF</span><span class="sxs-lookup"><span data-stu-id="a26a5-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a26a5-128"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="a26a5-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a26a5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a26a5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a26a5-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a26a5-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a26a5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a26a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a26a5-132">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="a26a5-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





