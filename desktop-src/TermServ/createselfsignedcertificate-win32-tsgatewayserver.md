---
title: Win32_TSGatewayServer 類別的 CreateSelfSignedCertificate 方法
description: 建立自我簽署憑證，並將憑證雜湊傳回為 \ 0034; out \ 0034;參數。
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- CreateSelfSignedCertificate 方法遠端桌面服務
- CreateSelfSignedCertificate 方法遠端桌面服務，Win32_TSGatewayServer 類別
- Win32_TSGatewayServer 類別遠端桌面服務，CreateSelfSignedCertificate 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464589"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="beabb-106">Win32 TSGatewayServer 類別的 CreateSelfSignedCertificate 方法 \_</span><span class="sxs-lookup"><span data-stu-id="beabb-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="beabb-107">建立自我簽署的憑證，並將憑證雜湊傳回為 "out" 參數。</span><span class="sxs-lookup"><span data-stu-id="beabb-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="beabb-108">此外，將「TS \_ 閘道 \_ 自我簽署憑證」文字新增 \_ \_ 至憑證內容屬性，以便將憑證辨識為遠端桌面閘道 (RD 閘道) 憑證。</span><span class="sxs-lookup"><span data-stu-id="beabb-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="beabb-109">這個方法會使用 RD 閘道特定的金鑰容器來建立憑證。</span><span class="sxs-lookup"><span data-stu-id="beabb-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="beabb-110">語法</span><span class="sxs-lookup"><span data-stu-id="beabb-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="beabb-111">參數</span><span class="sxs-lookup"><span data-stu-id="beabb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beabb-112">*SubjectName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="beabb-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beabb-113">自我簽署憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="beabb-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="beabb-114">*CertHash* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="beabb-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beabb-115">憑證雜湊。</span><span class="sxs-lookup"><span data-stu-id="beabb-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="beabb-116">備註</span><span class="sxs-lookup"><span data-stu-id="beabb-116">Remarks</span></span>

<span data-ttu-id="beabb-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="beabb-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="beabb-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="beabb-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="beabb-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="beabb-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="beabb-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="beabb-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="beabb-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="beabb-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="beabb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="beabb-122">Requirements</span></span>



| <span data-ttu-id="beabb-123">需求</span><span class="sxs-lookup"><span data-stu-id="beabb-123">Requirement</span></span> | <span data-ttu-id="beabb-124">值</span><span class="sxs-lookup"><span data-stu-id="beabb-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="beabb-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="beabb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="beabb-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="beabb-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="beabb-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="beabb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="beabb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="beabb-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="beabb-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="beabb-129">Namespace</span></span><br/>                | <span data-ttu-id="beabb-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="beabb-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="beabb-131">MOF</span><span class="sxs-lookup"><span data-stu-id="beabb-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beabb-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="beabb-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="beabb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="beabb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beabb-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beabb-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="beabb-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="beabb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beabb-136">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="beabb-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

