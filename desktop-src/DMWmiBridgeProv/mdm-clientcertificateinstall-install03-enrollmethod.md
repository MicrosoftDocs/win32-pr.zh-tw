---
title: MDM_ClientCertificateInstall_Install03 類別的 EnrollMethod 方法
description: 觸發裝置以啟動憑證註冊。
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- EnrollMethod 方法
- EnrollMethod 方法，MDM_ClientCertificateInstall_Install03 類別
- MDM_ClientCertificateInstall_Install03 類別，EnrollMethod 方法
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686192"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="b9116-106">MDM \_ ClientCertificateInstall Install03 類別的 EnrollMethod \_ 方法</span><span class="sxs-lookup"><span data-stu-id="b9116-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="b9116-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b9116-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9116-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b9116-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9116-109">觸發裝置以啟動憑證註冊。</span><span class="sxs-lookup"><span data-stu-id="b9116-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="b9116-110">憑證註冊完成後，裝置將不會通知 MDM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9116-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="b9116-111">MDM 伺服器稍後可以查詢裝置，以找出是否已新增新憑證。</span><span class="sxs-lookup"><span data-stu-id="b9116-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="b9116-112">另請參閱 [**註冊**](/windows/client-management/mdm/clientcertificateinstall-csp)。</span><span class="sxs-lookup"><span data-stu-id="b9116-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9116-113">語法</span><span class="sxs-lookup"><span data-stu-id="b9116-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="b9116-114">參數</span><span class="sxs-lookup"><span data-stu-id="b9116-114">Parameters</span></span>

<span data-ttu-id="b9116-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b9116-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9116-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9116-116">Return value</span></span>

<span data-ttu-id="b9116-117">必要。</span><span class="sxs-lookup"><span data-stu-id="b9116-117">Required.</span></span> <span data-ttu-id="b9116-118">觸發裝置以啟動憑證註冊。</span><span class="sxs-lookup"><span data-stu-id="b9116-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="b9116-119">憑證註冊完成後，裝置將不會通知 MDM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b9116-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="b9116-120">MDM 伺服器稍後可以查詢裝置，以找出是否已新增新憑證。</span><span class="sxs-lookup"><span data-stu-id="b9116-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9116-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9116-121">Requirements</span></span>



| <span data-ttu-id="b9116-122">需求</span><span class="sxs-lookup"><span data-stu-id="b9116-122">Requirement</span></span> | <span data-ttu-id="b9116-123">值</span><span class="sxs-lookup"><span data-stu-id="b9116-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9116-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9116-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9116-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9116-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9116-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9116-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9116-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="b9116-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b9116-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9116-128">Namespace</span></span><br/>                | <span data-ttu-id="b9116-129">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b9116-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b9116-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b9116-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9116-131"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9116-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9116-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b9116-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9116-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9116-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9116-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9116-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9116-135">**MDM \_ ClientCertificateInstall \_ Install03**</span><span class="sxs-lookup"><span data-stu-id="b9116-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="b9116-136">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="b9116-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

