---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetPortNumbers 方法
description: 設定允許透過遠端桌面閘道 (RD 閘道) 連接到資源的埠號碼。
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- SetPortNumbers 方法遠端桌面服務
- SetPortNumbers 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetPortNumbers 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465977"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="bcf9d-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetPortNumbers 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bcf9d-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="bcf9d-107">設定允許透過遠端桌面閘道 (RD 閘道) 連接到資源的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf9d-108">語法</span><span class="sxs-lookup"><span data-stu-id="bcf9d-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="bcf9d-109">參數</span><span class="sxs-lookup"><span data-stu-id="bcf9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf9d-110">*PortNumbers* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bcf9d-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf9d-111">此遠端桌面資源授權原則允許的以分號分隔的埠號碼清單， (RD RAP) 。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="bcf9d-112">若要允許任何埠號碼，請設定 " \* "。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcf9d-113">備註</span><span class="sxs-lookup"><span data-stu-id="bcf9d-113">Remarks</span></span>

<span data-ttu-id="bcf9d-114">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bcf9d-115">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bcf9d-116">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bcf9d-117">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="bcf9d-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf9d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcf9d-118">Requirements</span></span>



| <span data-ttu-id="bcf9d-119">需求</span><span class="sxs-lookup"><span data-stu-id="bcf9d-119">Requirement</span></span> | <span data-ttu-id="bcf9d-120">值</span><span class="sxs-lookup"><span data-stu-id="bcf9d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf9d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcf9d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf9d-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="bcf9d-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bcf9d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcf9d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf9d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcf9d-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bcf9d-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="bcf9d-125">Namespace</span></span><br/>                | <span data-ttu-id="bcf9d-126">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="bcf9d-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bcf9d-127">MOF</span><span class="sxs-lookup"><span data-stu-id="bcf9d-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcf9d-128"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9d-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcf9d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf9d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf9d-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9d-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bcf9d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcf9d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf9d-132">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="bcf9d-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

