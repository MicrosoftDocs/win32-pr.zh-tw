---
title: GetTSAudioEndpointEnumeratorForSession 回呼函式
description: 傳回指定之會話識別碼之音訊端點列舉值的參考。
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- GetTSAudioEndpointEnumeratorForSession 回呼函式遠端桌面服務
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106978602"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="f1819-104">GetTSAudioEndpointEnumeratorForSession 回呼函式</span><span class="sxs-lookup"><span data-stu-id="f1819-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="f1819-105">傳回指定之會話識別碼之音訊端點列舉值的參考。</span><span class="sxs-lookup"><span data-stu-id="f1819-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="f1819-106">此音訊端點列舉值的取用者（例如 MMDevAPI.dll）會呼叫此函式，以在遠端桌面服務會話中取出音訊端點列舉值。</span><span class="sxs-lookup"><span data-stu-id="f1819-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1819-107">語法</span><span class="sxs-lookup"><span data-stu-id="f1819-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="f1819-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1819-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1819-109">*SessionId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1819-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1819-110">遠端桌面服務會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1819-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="f1819-111">*ppEndpointEnumerator* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1819-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1819-112">[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="f1819-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1819-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1819-113">Return value</span></span>

<span data-ttu-id="f1819-114">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f1819-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1819-115">備註</span><span class="sxs-lookup"><span data-stu-id="f1819-115">Remarks</span></span>

<span data-ttu-id="f1819-116">標頭檔中未定義此函式。</span><span class="sxs-lookup"><span data-stu-id="f1819-116">This function is not defined in a header file.</span></span> <span data-ttu-id="f1819-117">您應該在自訂端點列舉值中執行並匯出此函式，並使用本主題稍早語法區塊中所示的簽章。</span><span class="sxs-lookup"><span data-stu-id="f1819-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1819-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1819-118">Requirements</span></span>



| <span data-ttu-id="f1819-119">需求</span><span class="sxs-lookup"><span data-stu-id="f1819-119">Requirement</span></span> | <span data-ttu-id="f1819-120">值</span><span class="sxs-lookup"><span data-stu-id="f1819-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="f1819-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1819-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1819-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="f1819-122">None supported</span></span><br/>         |
| <span data-ttu-id="f1819-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1819-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1819-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f1819-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1819-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1819-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1819-126">執行自訂音訊端點列舉值</span><span class="sxs-lookup"><span data-stu-id="f1819-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="f1819-127">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="f1819-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

