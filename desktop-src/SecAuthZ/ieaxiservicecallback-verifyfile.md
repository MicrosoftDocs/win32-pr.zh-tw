---
description: 針對指定的 ActiveX 物件執行安全性檢查，並傳回下載對應 .cab 檔案的位置。
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: IeAxiServiceCallback：： VerifyFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513913"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="97509-103">IeAxiServiceCallback：： VerifyFile 方法</span><span class="sxs-lookup"><span data-stu-id="97509-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="97509-104">**VerifyFile** 方法會在指定的 ActiveX 物件上執行安全性檢查，並傳回下載對應 .cab 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="97509-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="97509-105">語法</span><span class="sxs-lookup"><span data-stu-id="97509-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="97509-106">參數</span><span class="sxs-lookup"><span data-stu-id="97509-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97509-107">*bstrFileUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97509-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97509-108">要檢查之 ActiveX 物件的 URL。</span><span class="sxs-lookup"><span data-stu-id="97509-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="97509-109">*bstrApprovedFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="97509-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97509-110">已下載與 ActiveX 物件相關聯之 .cab 檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="97509-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97509-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="97509-111">Return value</span></span>

<span data-ttu-id="97509-112">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="97509-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="97509-113">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="97509-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="97509-114">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](/windows/desktop/SecCrypto/common-hresult-values)。</span><span class="sxs-lookup"><span data-stu-id="97509-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="97509-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="97509-115">Requirements</span></span>



| <span data-ttu-id="97509-116">需求</span><span class="sxs-lookup"><span data-stu-id="97509-116">Requirement</span></span> | <span data-ttu-id="97509-117">值</span><span class="sxs-lookup"><span data-stu-id="97509-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97509-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97509-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97509-119">Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97509-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97509-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97509-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97509-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="97509-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="97509-122">IID</span><span class="sxs-lookup"><span data-stu-id="97509-122">IID</span></span><br/>                      | <span data-ttu-id="97509-123">IID \_ IeAxiServiceCallback 定義為1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="97509-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="97509-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97509-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97509-125">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="97509-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

