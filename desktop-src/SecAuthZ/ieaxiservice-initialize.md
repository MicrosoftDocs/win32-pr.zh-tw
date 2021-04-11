---
description: 檢查和下載 ActiveX 物件。
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: IeAxiService：： Initialize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194934"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="4fc60-103">IeAxiService：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="4fc60-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="4fc60-104">**Initialize** 方法會檢查及下載 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="4fc60-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="4fc60-105">如果物件符合原則需求，這個方法會初始化安裝 ActiveX 物件的系統物件。</span><span class="sxs-lookup"><span data-stu-id="4fc60-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc60-106">語法</span><span class="sxs-lookup"><span data-stu-id="4fc60-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="4fc60-107">參數</span><span class="sxs-lookup"><span data-stu-id="4fc60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc60-108">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-109">嘗試安裝 ActiveX 控制項之視窗的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="4fc60-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="4fc60-110">*dwClientPID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-111">呼叫進程的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fc60-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="4fc60-112">*bstrDesktop* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-113">物件的桌面。</span><span class="sxs-lookup"><span data-stu-id="4fc60-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="4fc60-114">*bstrClsID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-115">要安裝之 ActiveX 物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fc60-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="4fc60-116">*bstrURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-117">要安裝之 ActiveX 物件的 URL。</span><span class="sxs-lookup"><span data-stu-id="4fc60-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="4fc60-118">*pbstrNonce* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-119">可以用來在呼叫其他方法時，用來共用狀態資訊的內容，用來驗證及下載 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="4fc60-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="4fc60-120">*ppISyncBrokerInterface* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc60-121">[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)介面的實例的指標，該介面會安裝 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="4fc60-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc60-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fc60-122">Return value</span></span>

<span data-ttu-id="4fc60-123">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4fc60-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="4fc60-124">如果函式失敗，則傳回值可以是下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4fc60-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="4fc60-125">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4fc60-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="4fc60-126">Description</span><span class="sxs-lookup"><span data-stu-id="4fc60-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="4fc60-127"><dt>**信任 \_電子 \_ 主體 \_ 不 \_ 受信任**</dt> <dt>0x800B0004</dt></span><span class="sxs-lookup"><span data-stu-id="4fc60-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="4fc60-128">不應安裝 ActiveX 物件。</span><span class="sxs-lookup"><span data-stu-id="4fc60-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4fc60-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fc60-129">Requirements</span></span>



| <span data-ttu-id="4fc60-130">需求</span><span class="sxs-lookup"><span data-stu-id="4fc60-130">Requirement</span></span> | <span data-ttu-id="4fc60-131">值</span><span class="sxs-lookup"><span data-stu-id="4fc60-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc60-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fc60-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc60-133">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fc60-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4fc60-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fc60-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc60-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="4fc60-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="4fc60-136">IID</span><span class="sxs-lookup"><span data-stu-id="4fc60-136">IID</span></span><br/>                      | <span data-ttu-id="4fc60-137">IID \_ IeAxiService 定義為 E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="4fc60-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4fc60-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fc60-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc60-139">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="4fc60-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




