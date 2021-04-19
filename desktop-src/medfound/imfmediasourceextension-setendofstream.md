---
description: 指出已到達媒體資料流程的結尾。
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: IMFMediaSourceExtension：： SetEndOfStream 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982143"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="413ae-103">IMFMediaSourceExtension：： SetEndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="413ae-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="413ae-104">指出已到達媒體資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="413ae-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="413ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="413ae-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="413ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="413ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="413ae-107">*錯誤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="413ae-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="413ae-108">用來傳遞錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="413ae-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="413ae-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="413ae-109">Return value</span></span>

<span data-ttu-id="413ae-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="413ae-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="413ae-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="413ae-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="413ae-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="413ae-112">Requirements</span></span>



| <span data-ttu-id="413ae-113">需求</span><span class="sxs-lookup"><span data-stu-id="413ae-113">Requirement</span></span> | <span data-ttu-id="413ae-114">值</span><span class="sxs-lookup"><span data-stu-id="413ae-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="413ae-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="413ae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="413ae-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="413ae-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="413ae-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="413ae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="413ae-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="413ae-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="413ae-119">Idl</span><span class="sxs-lookup"><span data-stu-id="413ae-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="413ae-120"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="413ae-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="413ae-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="413ae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="413ae-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="413ae-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="413ae-123">**MF \_ MSE \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="413ae-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




