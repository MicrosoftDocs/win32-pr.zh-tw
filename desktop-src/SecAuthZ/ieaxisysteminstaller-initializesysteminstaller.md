---
description: 安裝指定的 ActiveX 物件。
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: IeAxiSystemInstaller：： InitializeSystemInstaller 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851696"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="69fcb-103">IeAxiSystemInstaller：： InitializeSystemInstaller 方法</span><span class="sxs-lookup"><span data-stu-id="69fcb-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="69fcb-104">**InitializeSystemInstaller** 方法會安裝指定的 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="69fcb-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fcb-105">語法</span><span class="sxs-lookup"><span data-stu-id="69fcb-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="69fcb-106">參數</span><span class="sxs-lookup"><span data-stu-id="69fcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69fcb-107">*bstrUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69fcb-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69fcb-108">要安裝之 ActiveX 物件的 URL。</span><span class="sxs-lookup"><span data-stu-id="69fcb-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="69fcb-109">*dwClientPID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69fcb-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69fcb-110">呼叫進程的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="69fcb-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="69fcb-111">*pCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69fcb-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69fcb-112">[**IeAxiServiceCallback**](ieaxiservicecallback.md)介面實例的指標，該介面會驗證是否允許安裝 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="69fcb-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="69fcb-113">*pbstrNonce* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="69fcb-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69fcb-114">可以用來在呼叫其他方法時，用來共用狀態資訊的內容，用來驗證及下載 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="69fcb-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69fcb-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="69fcb-115">Return value</span></span>

<span data-ttu-id="69fcb-116">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="69fcb-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="69fcb-117">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="69fcb-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="69fcb-118">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](/windows/desktop/SecCrypto/common-hresult-values)。</span><span class="sxs-lookup"><span data-stu-id="69fcb-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="69fcb-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="69fcb-119">Requirements</span></span>



| <span data-ttu-id="69fcb-120">需求</span><span class="sxs-lookup"><span data-stu-id="69fcb-120">Requirement</span></span> | <span data-ttu-id="69fcb-121">值</span><span class="sxs-lookup"><span data-stu-id="69fcb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69fcb-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69fcb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="69fcb-123">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69fcb-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="69fcb-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69fcb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="69fcb-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="69fcb-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="69fcb-126">IID</span><span class="sxs-lookup"><span data-stu-id="69fcb-126">IID</span></span><br/>                      | <span data-ttu-id="69fcb-127">IID \_ IeAxiSystemInstaller 定義為 a50ea6f8-4764-4299-b309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="69fcb-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="69fcb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69fcb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69fcb-129">**IeAxiSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="69fcb-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

